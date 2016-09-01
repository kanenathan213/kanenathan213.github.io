---
layout: post
title:  "A Better Way to Connect Optimizely experiments to Heap"
date:   2016-08-30
categories: software
author: "Nathan Kane"
featured: true
comments: true
---

--------
<br>
[Heap](https://heapanalytics.com/) is a pretty revolutionary approach to analytics, providing lots of tracking for very little instrumentation work. However, one customization that my team found necessary was to link active Optimizely experiments to Heap behavior tracking, so we could set up funnels and segments based on who saw which experiment.

The [Heap documentation](https://heapanalytics.com/docs/using-identify) provides the way to do this. However, in implementing this into my project, I suspected there was a more expressive and error-proof way to write this method.

Here's the snippet they provide to build an object of Optimizely experiments and send them to Heap.

{% highlight javascript %}

// Create an object to store experiment names and variations
var props = {}

for (idx in optimizely.activeExperiments) {
    props[optimizely.data.experiments[optimizely.activeExperiments[idx]].name]
    = optimizely.variationNamesMap[optimizely.activeExperiments[idx]];
}
heap.addUserProperties(props)

{% endhighlight %}

My first issue is that using `for...in` for looping through an array (`optimizely.activeExperiments`) is a bit of an antipattern. Given that, in arrays, sequence usually matters, `for...in` can be misleading since there's no guarantee you'll get the order you expect. [Mozilla's docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) provide a more thorough explanation. Plus, our linter really didn't like `for...in`, not that I should always let linters boss me around :).

Collection order may not matter so much here, but I found `reduce` a more natural fit for extracting values from an array to build up an object.

Second, maybe I'm paranoid, but creaing a critical dependency on two asynchronously-loaded analytics libraries (Heap and Optimizely) scares me. This fear was validated in testing when this method broke on pages where Optimizely was deactivated, or no active experiments were present. So, I found the use of `try...catch` and existence checks for the libraries justified.

Finally, I had to do quite a bit of debugging and inspecting to discover what each value actually was. `idx` is not a helpful variable name (turns out that it corresponds to the current index in the `activeExperiments` array). Sure, the snippets end up being only a few lines of code, but the deeply chained collection accessing made my head hurt. I sought to address this readability concern with some clarifying variable assignments.

Here's what I came up with:

{% highlight javascript %}

try {
  if (heap && optimizely && optimizely.activeExperiments.length > 0) {
    // Create an object to store experiment names and variations
    const props = optimizely.activeExperiments.reduce((accumulator, activeExperimentID) => {
    const experimentName = optimizely.data.experiments[activeExperimentID].name;
    const experimentVariationName = optimizely.variationNamesMap[activeExperimentID];
    accumulator[experimentName] = experimentVariationName;
    return accumulator;
  }, {});
  // Send to Heap
  heap.addUserProperties(props);
  }
} catch (error) {
  // handle error
} finally {
  // continue the flow
}

{% endhighlight %}

## Wrapping up
It's often easy and tempting to just copy-and-paste vendor code you're given. However, in this project, I learned that reading, understanding, and potentially revising library code to fit into your own project's style and conventions greatly helps readability and consistency, and means you can leverage the awesome new language features you have available.
