---
layout: post
title:  "BOOK NOTES: Clean Code"
date:   2016-02-21
categories: book-notes
author: "Nathan Kane"
featured: 'true'
comments: true
---
I've been reading a lot of programming books lately, and wanted to share gems I'm finding in them.  (I was shamelessly inspired by [Derek Sivers](https://sivers.org/book) for this).

BOOK: Clean Code

AUTHOR: Robert Martin.

[BUY IT](http://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship-ebook/dp/B001GSTOAM/)

Here are my favorite excerpts:

> In software, 80% or more of what we do is quaintly called “maintenance”: the act of repair. Rather than embracing the typical Western focus on producing good software, we should be thinking more like home repairmen in the building industry, or auto mechanics in the automotive field.

> Knowing where things are—using approaches such as suitable naming—is crucial.

> A place for everything, and everything in its place. A piece of code should be where you expect to find it—and, if not, you should re-factor to get it there.

> Making your code readable is as important as making it executable.

> The architect Christopher Alexander—father of patterns and pattern languages—views every act of design itself as a small, local act of repair.  

> Quality is the result of a million selfless acts of care—not just of any great method that descends from the heavens. That these acts are simple doesn’t mean that they are simplistic, and it hardly means that they are easy. They are nonetheless the fabric of greatness and, more so, of beauty, in any human endeavor. To ignore them is not yet to be fully human.

> There are two parts to learning craftsmanship: knowledge and work. You must gain the knowledge of principles, patterns, practices, and heuristics that a craftsman knows, and you must also grind that knowledge into your fingers, eyes, and gut by working hard and practicing.

> Learning to write clean code is hard work. It requires more than just the knowledge of principles and patterns. You must sweat over it. You must practice it yourself, and watch yourself fail. You must watch others practice it and fail. You must see them stumble and retrace their steps. You must see them agonize over decisions and see the price they pay for making those decisions the wrong way.

> Remember that code is really the language in which we ultimately express the requirements. We may create languages that are closer to the requirements. We may create tools that help us parse and assemble those requirements into formal structures. But we will never eliminate necessary precision—so there will always be code.

> LeBlanc’s law: Later equals never.

> The managers and marketers look to us for the information they need to make promises and commitments; and even when they don’t look to us, we should not be shy about telling them what we think.

> Bad code tempts the mess to grow! When others change bad code, they tend to make it worse.

> Like a good novel, clean code should clearly expose the tensions in the problem to be solved.

> Clean code can be read, and enhanced by a developer other than its original author. It has unit and acceptance tests. It has meaningful names. It provides one way rather than many ways for doing one thing. It has minimal dependencies, which are explicitly defined, and provides a clear and minimal API.

> The next time you write a line of code, remember you are an author, writing for readers who will judge your effort.

> The ratio of time spent reading vs. writing [code] is well over 10:1.

> Making code easy to read actually makes it easier to write.

> If we all checked-in our code a little cleaner than when we checked it out, the code simply could not rot.

> The name of a variable, function, or class, should answer all the big questions. It should tell you why it exists, what it does, and how it is used. If a name requires a comment, then the name does not reveal its intent.

> Methods should have verb or verb phrase names like postPayment, deletePage, or save. Accessors, mutators, and predicates should be named for their value and prefixed with get, set, and is

> The hardest thing about choosing good names is that it requires good descriptive skills and a shared cultural background. This is a teaching issue rather than a technical, business, or management issue. As a result many people in this field don’t learn to do it very well.

> The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.

> Every function in this program was just two, or three, or four lines long. Each was transparently obvious. Each told a story. And each led you to the next in a compelling order. That’s how short your functions should be!

> This implies that the blocks within if statements, else statements, while statements, and so on should be one line long. Probably that line should be a function call. Not only does this keep the enclosing function small, but it also adds documentary value because the function called within the block can have a nicely descriptive name.

> The indent level of a function should not be greater than one or two. This, of course, makes the functions easier to read and understand.

> FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY.

> A long descriptive name is better than a short enigmatic name. A long descriptive name is better than a long descriptive comment.

> Functions should either do something or answer something, but not both. Either your function should change the state of an object, or it should return some information about that object. Doing both often leads to confusion.

> Writing software is like any other kind of writing. When you write a paper or an article, you get your thoughts down first, then you massage it until it reads well. The first draft might be clumsy and disorganized, so you wordsmith it and restructure it and refine it until it reads the way you want it to read.

> When I write functions, they come out long and complicated. They have lots of indenting and nested loops. They have long argument lists. The names are arbitrary, and there is duplicated code. But I also have a suite of unit tests that cover every one of those clumsy lines of code.

> So then I massage and refine that code, splitting out functions, changing names, eliminating duplication. I shrink the methods and reorder them. Sometimes I break out whole classes, all the while keeping the tests passing.

> In the end, I wind up with functions that follow the rules I’ve laid down in this chapter. I don’t write them that way to start. I don’t think anyone could.

> The proper use of comments is to compensate for our failure to express ourself in code.

> Every time you express yourself in code, you should pat yourself on the back. Every time you write a comment, you should grimace and feel the failure of your ability of expression.

> When people look under the hood, we want them to be impressed with the neatness, consistency, and attention to detail that they perceive. We want them to be struck by the orderliness. We want their eyebrows to rise as they scroll through the modules. We want them to perceive that professionals have been at work. If instead they see a scrambled mass of code that looks like it was written by a bevy of drunken sailors, then they are likely to conclude that the same inattention to detail pervades every other aspect of the project.

> You should take care that your code is nicely formatted. You should choose a set of simple rules that govern the format of your code, and then you should consistently apply those rules.

> Code formatting is about communication, and communication is the professional developer’s first order of business. Perhaps you thought that “getting it working” was the first order of business for a professional developer. I hope by now, however, that this book has disabused you of that idea. The functionality that you create today has a good chance of changing in the next release, but the readability of your code will have a profound effect on all the changes that will ever be made.

> Aim for 200-500 lines of code per file.

> We would like a source file to be like a newspaper article. The name should be simple but explanatory. The name, by itself, should be sufficient to tell us whether we are in the right module or not. The topmost parts of the source file should provide the high-level concepts and algorithms. Detail should increase as we move downward, until at the end we find the lowest level functions and details in the source file.
