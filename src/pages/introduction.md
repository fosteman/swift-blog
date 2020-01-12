---
path: /introduction/
title: My notes of Swift 5 language study: Idiomacy
image:
author: Timofei Shchepkin (Tim Fosteman)
category: Swift
tags: '#language #swift #development #code #blog'
---

# My notes of Swift 5 language study
## Idiomatic Swift
As a wretched perfectionist, I am tantalized to seek the correct way to do certain things. The standard library provides some clues, sure, but even that changed over time in C++, likewise in Swift (since 2.0 beta, yes, I am old enough to know the dropped conventions and adopted others). It was nearly 5 years ago since introduction of the language, and now, I am all in. 
~~Congratulate me, I require social approval to keep on going.~~

As a person coming from different language, 
Swift resembles everything likable from C++, low-level twiddling, 
yet rooted out undefined behaviours (think *null pointer exceptions*). 
The lightweight trailing closure syntax of `map` or `filter` are similar to that of **Ruby**.
Generics are similar C++ templates with additional type constraints to ensure generic functions integrity at the time of definition rather than runtime.
Flexible higher order functions and operator overloading means I can write code that's similar to JavaScript!
And the `@objc` and `dynamic` keywords allow me to use selectors and runtime dynamism in ways I could in Objective-C, **Wonderful**.

Given all that familiarity, I thought I could adopt all the same mental models from knowledge I have. Well, I am, indeed, capable of doing so, for conversion of Objective-C into Swift is 1 click away. Case point: familiar Object Oriented Design patterns apply.

I started coding... And hit a wall. Several times. I can't use protocol extensions with associated types like interfaces in Java (Arrays are not covariant). `functor` isn't here either. Thought, sure enough, there are ways of doing everything in a different manner.

Swift is a programming language unlike any one else, and this is promising, for it bring together the best practices, or so it says. (At least I need not to call C libraries to write a collection type).

### Thus I am into learning this language.
To write succinct, elegant code, get things in Apple application development done.

### This series of articles is about my journey. 

I promise to answer as many "Why does Swift behave like that?" as I may muster.  
Each article will cover fundamental concepts like optionals and strings one by one.