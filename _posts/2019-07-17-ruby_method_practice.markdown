---
layout: post
title:      "Ruby Method Practice"
date:       2019-07-17 14:22:47 +0000
permalink:  ruby_method_practice
---


As I prepare for coding challenges, I have been doing a lot of practice problems on sites like Code Wars and Hackerrank. I've been brushing up on my Ruby methods - here are a few I've focused on this week:

`.shift`
Removes the first element of an array and returns it. 
*Important to remember that the first element is returned! 

Example: 
`letters = ["a", "b", "c"]
letters.shift #=> "a"
letters #=> "["b", c"]`

`.each`
Calls the block for each element in the array and returns the array. 

`letters = ["a", "b", "c"]
letters.each {|char| print char}

#=> a, b, c`

`.reverse_each`
Same as `.each` but results are in reverse order.

`letters = ["a", "b", "c"]
letters.reverse_each {|char| print char}

#=> c, b, a`

.unshift

.group_by

.select()
