# My notes of Swift 5 language study
## Overview of themes

### Swift bridges multiple levels of abstraction
Swift is a high-level language - it allows one to write code similar to Python or Javascript, featuring HOCs like `map`, `reduce`. It's compiled directly into native libraries with performance (as it is said) similar to C.

It boils down to wonders of having loops and mapping closures to be as fast, thanks to very similar output assembly code.

Which comes to that it's very advisable to get around wisely choosing structs over classes, dynamic and static dispatch methods and correct pointer manipulation ~~(although, hopefully, it'll not descend that deep. No guarantees!)~~

### Swift is a multi-paradigm language

Swift allows to write object oriented code, or purely functional one using immutable values (yes, I'll discuss `let` vs `var`, too). I can also write imerative C-like code using pointer arithmetics! ~~(yay!)~~

This is impressive, yet, daunting. Swift features number of tools but does not force programmer to write a certain way,
it is a middle way.

As a successor to Objective C, most capabilities are maintained. So I can transgress Objective C to Swift in 1 click. Meaning message sending, runtime type identification, and keyvalue observation - all included. 
Swift, therefore, is a good introduction to a more functional style of programming through its use of generics, protocols, value types, and closures. Though preference of writing imperatively incorporating functional programming patterns is in the community's house. 

### Swift is flexible

I mentioned this notion of `bottom-up` approach to Swift, for it's fairly easy to write very generic building blocks, like primitives, trailing closures, to be combined into larger features. So, language evolves with the solution to the problem.

### Swift code is succinct

Swift can be written very tersely, comparably to that of JS scribblings. The underlying goal isn't to save on typing, however. I mentioned. that the idea is to get the the point quicker and to make code readable by dropping a lot of the "ceremonial" boilerplate that only obscures the meaning. 

Type inference is one example. Clutter of type declarations is removed. Semi-colons and parantheses, too, gone. Generics and protocol extensions encourage to follow DRY principle (DO NOT REPEAT YOURSELF) by packaging common operations into reusable functions. 

Voila, code's readable at a glance.

### Swift tries (and fails) to be as safe as it possible can

As I have found out, unlike dangerously-typed C, C++, and overly safe Java, 
Swift is something in between. It avoids undefined and unsafe behaviour by default. 

A Variable cannot be used until it's initialized, and using out-of-bounds subscripts on an array will fail to compile.

However, unsafe options are available. Examples are `unsafeBitCast` function, and the `UnsafeMutablePointer` type. 

Consider the following code that compiles, yet performs an allowed illegal move
```$swift
var someArray = [1, 2, 3]
let betterNot = someArray.withUnsafeBufferPointer {
    ptr in
    return ptr
   }
// Rock n' roll!
print(betterNot[10])
```
Democracy in action.

### Swift is opinionated

As I have read several sources of guidelines and design patterns attenuated to Swift, I sensed this strong opinionated air around them. 
As authors explain, Swift is still young and developing language, so they abstain from complete self-righteousness on the topic regardless.
 

### Swift continues to evolve

Major yearly syntax changes are behind this new decade (2020 Yay!), yet important areas of the language are still unfinished (string APIs, generic system, reflection, concurrency).
