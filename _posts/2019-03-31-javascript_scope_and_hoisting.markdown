---
layout: post
title:      "Javascript Scope and Hoisting"
date:       2019-03-31 16:28:14 -0400
permalink:  javascript_scope_and_hoisting
---


In Javascript, it is important to know when different variables and functions are available to your program. Two concepts that go hand in hand with variables are scope and hoisting. 

**SCOPE**

Javascript has three types of scope: **global** and **function** and **block**. Any variable declared outside of a block, or a function, is available to the entire program. For example:

```
let a = "Apple"
```

This variable is a **global** variable and, if declared outside of a function, is available anywhere in the program.

Variables that are declared without using ```var```, ```let```, or ```const``` are always in the global scope regardless of where they are originally declared. 

A variable declared within a function is in the **function scope**.  These variables can either be **blocked scoped** or not, depending on how the variable is declared. For example:

```
function newFunction() {
 let b = "Banana"
 console.log("b")
}
```

versus:

```
function newFunction() {
 var b = "Banana"
 console.log("b")
}
```


When a variable is declared within a block using either ```let``` or ```const```, it is **block scoped** and stays within the block (between the curly braces). If you tried to called the varaible elsewhere in the program, an error would be thrown stating that the variable is undefined. However, if the variable is declared using ```var```, it is only **function scoped** and, if called elsewhere, would return the value. It is better practice to declare variables using ```let``` or ```const``` to avoid confusion and code that is difficult to debug.


**HOISTING**

Hoisting is another concept that is important to understand in order to avoid bugs in your code. There are two types of hoisting: function hoisting and variable hoisting. 

*Function Hoisting*

Function hoisting refers to when a function is available in the two phases of the Javascript running. In the compilation phase, function invocations are ignored, and all function declarations are saved into the memory. During the execution phase, the browser already has a memory of the functions that have been declared, so the order in which they are referenced doesn't matter. For example:

```
function anotherFunction() {
 return "I'm a function"
}

anotherfunction()
```

and 

```
anotherfunction()

function anotherFunction() {
 return "I'm a function"
}
```

would run in exactly the same way. The function declarion is hoisted to the top and is saved in the memory. 

While both of these work the same, it's better practice to declare functions at the top of the code so it's easier to keep track of. 

*Variable Hoisting*

If a variable is declared with ```let``` or ```const``` after the variable is called in your code, an error message will be thrown telling you that you have yet to declare the variable. 

Example A:
```
function yetAnotherFunction() {
 let apple = banana;
 console.log(apple);
}

//LOG: banana
```

Example B:
```
function yetAnotherFunction() {
 console.log(apple);
 let apple = banana;
}

//LOG: Error - apple has not been declared.
```

However, if you use ```var``` instead of ```let```, the declaration is hoisted to the top and comes back as "undefined" rather than throwing an error. 

Example C:
```
function yetAnotherFunction() {
 console.log(apple)
 var apple = banana
}

//LOG: apple is undefined. 
```

This makes it difficult to keep track of when the variables have been defined and it is best practice to either use ```let``` or ```const``` when defining variables. This helps avoid this example of hoisting and keeps all of your variable declarations at the top of your code. 






