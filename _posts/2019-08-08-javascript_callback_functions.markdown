---
layout: post
title:      "Javascript Callback Functions"
date:       2019-08-08 16:18:19 -0400
permalink:  javascript_callback_functions
---

Lately I've been reading "Secrets of a Javascript Ninja" and I found myself getting tripped up reading about callback functions. 

Turns out, I was making this out to be way more complicated than it is. 

Simply put, a callback function is a function that is called as an argument to another function and is executed after the first function has run. 

For example:
	
function sayHello(name, callback) {
 alert(`Hello, ${name}!`);
 callback();
 }
 
 sayHello('Heidi', function() {
  alert("Nice to meet you!");
	});

If you run this in your console (open the Javascript Console in your developer tools), you'll get 2 alerts: 

"Hello, Heidi"

"Nice to meet you!"

Super cool! The sayHello function ran first, and then called back the next function to say "Nice to meet you!" What a friendly program we've started! :)

It can be easy to get caught up in all of the punctuation and complexity of Javascript, but when you break it down piece by piece, it's often not nearly as complicated as it seems. 
	
	

