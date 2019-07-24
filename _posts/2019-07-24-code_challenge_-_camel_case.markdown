---
layout: post
title:      "Code Challenge - Camel Case"
date:       2019-07-24 16:56:52 -0400
permalink:  code_challenge_-_camel_case
---

One of my favorite ways of prepping for technical interviews has been solving various code challenges on popular sites. It's such a rush to see all of the tests passing! 

With my final project at Flatiron being so focused on React and Redux, I was out of practice with basic Ruby methods. One of the skills I've had to work on since graduating is reminding myself how to walk through a problem and figure out the solution. 

Here's how I solved a recent challenge:

`Take a string and convert to Camel Case so that the first letter of each word is capitalized without spaces .`

My first step would be plan out my solution. What is it I'm trying to do?

1. Put the individual words into an array
2. Capitalize the first letter of each word in the array
3. Join the words back into a string with no spaces

So if step 1 is to split the string into an array, let's use the `.split` method:

`def camelcase(string)<br>
 string.split(" ")<br>
end`

I used the example string "hello there" as my practice string. When I run this in an IDE, this method returns:

`["hello", "there"]`

Great! Now that I have the individual words in an array, I can map over them to capitalize the first letter. Fortunately, Ruby has a built-in method that will do this for me:

`def camelcase(string)
 string.split(" ").map {|word| word.capitalize}
end`

This returns:

`["Hello", "There"]`

Awesome! Now I just need to join the words together back into a string with no spaces!

`def camelcase(string)
 string.split(" ").map {|word| word.capitalize}.join("")
end`

What does it return? Exactly what we were looking for!

`HelloThere`

Doing a few of these a day will really improve your skills for thinking on your feet and problem solving. I can't wait to share more! 






