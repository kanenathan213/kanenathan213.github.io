---
layout: post
title:  "Software terms that tripped me up"
categories: software
author: "Nathan Kane"
date:   2016-03-01 13:33:54 -0800
---

KeyPath
--------

Here is some code:
{% highlight javascript %}

let nested_object = {
  a: {
    b: {
      c: {
        d: 5
      }
    }
  }
}

// Here is our KeyPath

let value_of_d = nested_object.getIn(['a','b','c','d']);

console.log(value_of_d)
// result: 5;

{% endhighlight %}

This is pattern I've come across using [ImmutableJS](https://facebook.github.io/immutable-js/)
