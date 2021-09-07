# Functional Programming

![](https://miro.medium.com/max/1400/1*1OxglOpkZHLITbIKEVCy2g.jpeg)

## What is functional programming?

**Functional programming** (often abbreviated FP) is the process of building software by composing **pure functions**, avoiding **shared state, mutable data,** and **side-effects**. 

Functional programming is **declarative** rather than **imperative**, and application state flows through pure functions. 

Contrast with object oriented programming, where application state is usually shared and colocated with methods in objects.


## What is a pure function and how do we know if something is a pure function?

A **pure function** is a function which:

* Given the same inputs, always returns the same output, and
* Has no side-effects

Pure functions have lots of properties that are important in functional programming, 

including referential transparency (you can replace a function call with its resulting value without changing the meaning of the program)

## What are the benefits of a pure function?

* They’re easier to reason about
* They’re easier to combine
* They’re easier to test
* They’re easier to debug
* They’re easier to parallelize
* They are idempotent
* They offer referential transparency
* They are memoizable
* They can be lazy

## What is immutability?
An immutable object is an object that can’t be modified after it’s created. Conversely, a mutable object is any object which can be modified after it’s created.

Immutability is a central concept of functional programming because without it, the data flow in your program is lossy. 

State history is abandoned, and strange bugs can creep into your software. 

## What is Referential transparency?


Referential transparency, a term commonly used in functional programming, means **that given a function and an input value, you will always receive the same output.** 

That is to say there is no external state used in the function




## What is a module?

A module is a software component or part of a program that contains one or more routines. One or more independently developed modules make up a program. 

An enterprise-level software application may contain several different modules, and each module serves unique and separate business operations.

Modules make a programmer's job easy by allowing the programmer to focus on only one area of the functionality of the software application. 

Modules are typically incorporated into the program (software) through interfaces.

## What does the word ‘require’ do?
In NodeJS, require() is a built-in function to include external modules that exist in separate files. 

require() statement basically reads a JavaScript file, executes it, and then proceeds to return the export object. 

require() statement not only allows to add built-in core NodeJS modules but also community-based and local modules.

**Syntax:**

To include a module, the require() function is used with the name of the module:

       var myVar = require('http'); //to use built-in modules

       Var myVar2 = require('./myLocaModule') to use local modules

## How do we bring another module into the file the we are working in?

![ ](https://www.stanleyulili.com/assets/images/posts/node-featured-image/featured-image.jpg )

to maintain, reuse and organize code, you need to split the code into multiple files. 

This process is called modularization. Each module contains functions or classes that handle a specific functionality.

Functions in one module can be imported and called in other modules saving you from having to copy function definitions into the other files. 

A module can be edited or debugged separately making it easier for you to add or remove new features.

In this tutorial, you will learn how to create Node.js modules. You will also learn how to include functions defined in one file and use them in another file


## What do we have to do to make a module available?

To use the functionality present in any module, you have to import it into your current program. You need to use the import keyword along with the desired module name. 

When interpreter comes across an import statement, it imports the module to your current program.












