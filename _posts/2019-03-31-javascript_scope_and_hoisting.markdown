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

Any time you called "a" within your program, it would return "Apple."

A variable declared within a function is in the function scope. For example:

```
function newFunction() {
 var b = Banana
 console.log("b")
}
```

In these two examples, the variable "a" is available anywhere ("globally") in the program. The variable "b" is only available within newFunction() and cannot be referred to outside of the function. If you tried to use "b" in another part program, you would see an error message that "b" has not been declared.

The exception would be if the variable within the function was declared without using var, let, or const:

```
function newFunction() {
 b = Banana
 console.log("b")
}
```

Even though this is declared within newFunction(), it was not declared using var, let, or const and is automatically a global variable. This makes it difficult to keep track of variables and should be avoided wherever possible.

Starting in ES2015, block scoping is partially available. This means that a block can support scope, as long as you use let and const. 

For example:

```
if (true) {
 let a = Apple;
 const b = Banana;
}	
```

If you tried to call either a or b, they would come back as undefinied since they are contained within the block. 

However, block scoping does not variables declared with var. In this example, 

```
if (true) {
     var c = Cat;
}
```

calling c would return "Cat", not undefined. This makes it difficult to keep track of variables, so it's always preferred to use let and const. 


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

Variable hoisting is simliar to function hoisting, but if a variable is declared with let or const before the variable is called, an error message will be thrown telling you that you have yet to declare the variable. 

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

However, if you use var instead of let, the declaration is hoisted to the top and comes back as "undefined" rather than throwing an error. 

Example C:
```
function yetAnotherFunction() {
     console.log(apple)
		 var apple = banana
}

//LOG: apple is undefined. 
```

This makes it difficult to keep track of when the variables have been defined and it is best practice to either use let or const when defining variables. This helps avoid this example of hoisting and keeps all of your variable declarations at the top of your code. 






