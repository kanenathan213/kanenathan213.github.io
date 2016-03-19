---
layout: post
title:  "Coding as a Designer"
date:   2015-11-04
categories: general
author: "Nathan Kane"
featured: true
comments: true
---
I became convinced to that coding ought to become a part of my design process after reading [Why We Skip Photoshop](https://signalvnoise.com/posts/1061-why-we-skip-photoshop) by Basecamp founder/CEO Jason Fried. In it, he explains their rationale for skipping graphic design tools in favor of developing in the browser. At reading it for the first time, I had visions of painfully positioning boxes on a screen at a snail's pace, and having to Google every minor change. However, over time, code has become my default way to whip up mockups and prototypes quickly, producing higher quality and (actually) useful artifacts at the end of my process.

Designing in code is about raising the level of fidelity for communication purposes: to your peers, customers, even investors, to guide your own creative intuition. Fidelity usually comes with the cost of time and effort, exerting more refinement and thought over implementation. Coding does require more keystrokes and clarity of thought than simply drawing a design in Sketch or Photoshop. But, the clickability and aliveness you get with the finished product are benefits that outweigh this cost. Plus, you end up usually with a skeleton of code for someone (either you or your engineer) to start writing production code with, copying some lines of code, or just seeing one implementation direction.

The point is that by making coding a routine part of your process, you will naturally increase your defness, like learning any tool. We all started excruciatingly slow with our favorite design tool (especially if it's Photoshop), but over time, it feels light and obedient. The same goes with coding: after the learning curve, the speed can match that of a graphical tool. Moreover, you'll gain an appreciation for what your dev team does, and for what's hard and what's 'free' when considering design directions.

## Why now?

It's amazing that Basecamp was pioneering this back in mid-2008(!), before many of the tools that power UI development existed. Now, with the proper tooling and knowledge, one can produce visual interfaces more rapidly than ever before. Plus, the output front-end code can be close to production-ready. Even more important, with responsiveness, I'd argue it's easier to design in the browser, where you can simply resize it to get certain adaptations of your work. This wasn't an issue in 2008, but it is fundamental now, and easier to do than ever.

Plus, the knowledge to get started is so readily available. Github has a boilerplate or seed repo to kickoff a project; NPM/Bower/Gulp take care of dependencies and tooling; Stack Overflow has the answer to your question; and Udacity, Lynda, or Treehouse can, Matrix-like, update your brain with a lesson on the latest technology. Where it probably took months for a non-technical designer to pick up any front-end code, now it's a couple weekends and side projects before you'll feel comfortable. Soon, you'll learn enough to get into learning escape velocity, where you can't help but compound your knowledge because you're building things with the basics, and prodding the tool to do more.

That said, there is an infinite amount of knowledge, tools, frameworks, fashions, and techniques in the UI world, and more every day. It can be daunting, and make you constantly feel underskilled. Just distilling the current, more applicable ones was a challenge in getting myself into UI development. So, I've tried to assemble and sequence the bare bones skills to pick up to get you on a glidepath to designing in code.

## What to focus on as a new-to-code designer

Start with a focus on prototyping. This will put coding right in your wheelhouse of design work, giving you immediate feedback and satisfaction with things like nifty animations. This means basic HTML, along with CSS and CSS3 animations. I'd recommend just starting with Bootstrap in your first project so components look passable (albeit generic), and overriding when you want to customize. Opening up your file in the browser and firing up Chrome devtools (Cmd-option-I on a Mac), the Chrome browser is now your new design playground. Inspect all the things (Cmd-option-C)!

One you start getting annoyed by redundant CSS, you'll probably want to start using Sass, the most popular CSS preprocessor, for things like variable, mixins, and nesting.

To start managing data in your prototype, and handling things like routing, I recommend using Angular 1.x. (You'll need to run a local webserver like http-server for these kinds of apps). Angular comes with tons of off-the-shelf modules for common use cases, like handling forms, looping through an array of data, and hiding or showing elements based on app state. I found Angular shielded me from a lot of the nastiness under the hood of browser-run Javascript, while still teaching me the Javascript basics I needed. If you really want to bravely venture out into the dev world, React is the new hotness with it's reusable component hierarchy (analagous to atomic design). It's overkill for most prototyping projects, but if you're working on an ongoing series of projects with share prototypes, it may be worth investing in creating a base app with one of these more complicated frameworks, and keep it modularized and reusable.

## TL;DR

Coding as a designer is easier than every before. It's all about selecting the appropriate skills and tools in the right order. By switching from static mockups to functional prototypes, you'll move more swiftly to a better endpoint in your design, and solicit more meaningful feedback.
