# My notes of Swift 5 language study
## Terminology

"When I use a word, it means what I choose it to mean - neither more nor less."
- Through the Looking Glass, by Lewis Carroll

### Distinction between values, variables, references, and constants.

A value is immutable. Alike lvalue or literals in C (e.g. `true`, `1`, `[1,2]`)

A variable is created `var variable = [1,2]`. Changes are possible `variable.append(3)`. The value is replaced with a new one. Also referrs to "Mutation"

Constants are declared using `let constant = [1, 2]`. New values are never assigned after initialization. Meaning, initialization maybe postponed, i.e. declaration `let a: Int` precedes the actual initializtion `a = 1`

Structs and enums are value types, i.e. one struct variable assigned to another will have the same value. Contents are copied, not referenced.

References point to things in memory, just like pointers in C.

#### Interoperability
Classes are reference types, although explicit deferencing of these "pointers" is syntactically sweetened with sugar. Class instances (objects) may not be held directly in variables, instead, a refernece is in a variable and access it is allowed via that reference.

Pointers are also reference types.

#### Structs and Classes
A variable that holds a reference is constant. 

Some classes are completely immutable - that is, they provide no methods for changing their internal state after they are created. 

Reference types have identity. Two variables are referring to the exact same object by using `===`. They are equal, assuming `==` is implemented for the type. 

Yes, two objects with different identities can still be equal.

Value types haven't an identity, hence particular variable does not hold the "same" value as another. But it may surely contain the value 2. 
`===` is really asking: "Do these variables hold the same reference to their value?"

`==` is referred to structural equality
`===` is called pointer equality or reference equality.

#### Functions

Functions are also values, they can be assigned to variables, have an array of functions, and call the function help in a variable. Higher order functions taking enclosures like `map`, and `sort` are present.

Functions may be declared using `func` keyword or with an unnamed closure expression `{}`

Functions are held by reference, meaning that, assigned a function tht has a captured state to another variable truly shares the held variable, similar to object references.

Functions defined inside a class or protocol are called **methods**, and they capture implicit `self` parameter. 

**Free functions** are defined outside of classes or protocols.

A fully qualified name in Swift includes the base name and arguement labels (i.e. `index(_: offsetBy:))` which indicates that `index` has two arguements, first one of which has no label.

Free functions and methods, called on structs, are statically dispatched (i.e. it's known at compile time). Good thing, optimizer can simplify code downsizing to inline functions.

Methods on classes or protocols might be dynamically dispatched via vtables, similarly to dynamic dispatch in C++).

#### Generics

Polymorphic behavior is attained with subtyping and method overriding. Behavior is thus modified depending on type involed. Function overloading is in the house, too. Generics, providing one implementation for any type, are also in the house. Both are known at compile time.