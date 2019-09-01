---
layout: post
title:      "Code Challenge - Odd Ones Out"
date:       2019-09-01 13:33:35 +0000
permalink:  code_challenge_-_odd_ones_out
---


Another week, another code challenge!

This week, my focus was on a challenge I'd tried to solve before but got stuck. The challenge is to write a method that takes an array of numbers and returns a new array of numbers that occured an equal number of times in the original array, without rearranging. For example:

odd_ones_out([4, 5, 4, 5, 8, 9, 4, 8] => [5, 5, 8, 8]

I found this problem challenging, particularly because of the requirement to keep the numbers in order. 

The first step was to create an empty hash called "counts" that would hold each number and it's corresponding count. 

def odd_ones_out(numbers)
 counts = {}
end

Next, I need to iterate over the numbers array and see if the number is already included in the counts hash. If it is, the number will increase by one. If it isn't, the number will start at 1. 

def odd_ones_out(numbers)
 counts = {}
 numbers.each{|i|
   if counts.include?(i)
	   counts[i] += 1
	else
     counts[i] = 1
	end
end

Now I just need to return the results! 

def odd_ones_out(numbers)
  counts = {}
  numbers.each{|i|
    if counts.include?(i)
      counts[i] += 1
    else
      counts[i] = 1
    end}
   numbers.select{|value|
     counts[value].even?}
end

It feels great to finally get this one solved! On to the next!

