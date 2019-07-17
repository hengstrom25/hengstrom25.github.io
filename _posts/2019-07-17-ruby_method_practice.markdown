---
layout: post
title:      "Ruby Method Practice"
date:       2019-07-17 10:22:48 -0400
permalink:  ruby_method_practice
---


As I prepare for coding challenges, I have been doing a lot of practice problems on sites like Code Wars and Hackerrank. I've been brushing up on my Ruby methods - here are a few I've focused on this week:

`.shift`
Removes the first element of an array and returns it. 
*Important to remember that the first element is returned! 

*Example: *
`letters = ["a", "b", "c"]
letters.shift #=> "a"
letters #=> "["b", c"]`

`.unshift`
Adds the new item to the front of the array

*Example:*
`letters = ["a", "b", "c"]
letters.unshift("d") #=> ["d", "a", "b", "c"]`

`.each`
Calls the block for each element in the array and returns the array. 

*Example:*
`letters = ["a", "b", "c"]
letters.each {|char| print char}

#=> a, b, c`

`.reverse_each`
Same as `.each` but results are in reverse order.

*Example:*
`letters = ["a", "b", "c"]
letters.reverse_each {|char| print char}

#=> c, b, a`

`.group_by`
Groups by the result of the block and returns a hash with the key as the result of the block and the values are the elements that correspond to the key. 

*Example:*


.select()
