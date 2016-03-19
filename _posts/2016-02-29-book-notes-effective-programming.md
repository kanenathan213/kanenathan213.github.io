---
layout: post
title:  "BOOK NOTES: Effective Programming"
date:   2016-02-29
categories: book-notes
author: "Nathan Kane"
featured: false
comments: true
---
Here are some of my most important takeaways from Jeff Atwood's book, Effective Programming
<br><br>


> Whatever the problem with your software is, take ownership. Start with your code, and investigate further and further outward until you have definitive evidence of where the problem lies.

Code often has countless dependencies—libraries, frameworks, API's—that are easy to blame when things go wrong. However, more likely, it's that your own code hasn't anticipate potential behavior of these dependencies by breaking gracefully. Or, you don't fully understand that dependency, which Atwood would fix by understanding any source code you depend on.
<br><br>


> Always write your code as if comments didn’t exist. This forces you to write your code in the simplest, plainest, most self-documenting way you can humanly come up with.

Some experts each go so far on this point as to discourage code comments, in an effort to pour more focus into writing expressive, understandable code. Atwood's helps formulate this into a mindset, of viewing your code in the eyes of those who will need to comprehend it later (which, often, will be future versions of yourself). It's also true that even when comments or documentation are written, they frequently are kept updated. Only the source code is the certain source of truth.
<br><br>



> If you’re not constantly obsessing over every aspect of your application, relentlessly polishing and improving every little part of it — no matter how trivial — you’re not executing. At least, not well.

This encapsulates why I got into development—the precision engineers exert on the details of an experience.
<br><br>



> All too often, software developers are merely tourists in their own codebase. Sure, they write the code, but they don’t use it on a regular basis like their customers do.

I don't know if 'dogfooding' is strong enough a word for constantly growing empathy for customers. All members of the product team should be starting (creating a new account) and using their product every week, ideally in a real-world way. Quickly, one notices the blemishes and friction in the product, and builds an emotional motivation for fixing those issues.
<br><br>



> I believe that peer code reviews are the single biggest thing you can do to improve your code.

Either through live pair programming, where one developer 'drives' and the other 'proofreads,' or just pre-merge comments and review, Atwood swears by getting a peer's eyes on your code.
<br><br>



> A/B testing is like sandpaper. You can use it to smooth out details, but you can’t actually create anything with it.

In a tech culture that holds A/B testing up as a panacea, this passage helped me step back and recognize that A/B testing is about optimization, not finding the ultimate best solution.
