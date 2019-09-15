---
layout: post
title:      "Whiteboard Interview"
date:       2019-09-15 13:40:11 +0000
permalink:  whiteboard_interview
---


A few weeks ago, I experienced my first whiteboard interview. Since the beginning of my coding journey, the whiteboard interview has seemed like the most intimidating interview experience. Here was my experience:

I spent the week before doing practice problems so I could practice thinking through different problems. When I got there, I was a little nervous but felt fairly confident in my ability to at least work on the problem. 

When it came time to do the whiteboard test, I made sure to talk through my thought process. My challenge was a compression problem and I made sure to ask questions before I started. I did a second example output so I could be sure I understood what I needed to do. 

It was a collaborative exercise. They asked me quesitons as I was going and we talked about what my code would do if it was run on a computer. We walked through it step by step and I made sure to explain when I was unclear about something. 

Once I finished the challenge, I felt pretty good about how I'd solved the problem. I went home and refactored the solution so it was the most efficient way to solve the problem. 

My solution was as follows:

[a,a,b,b,b,c,c] => [a,2,b,3,c,2]
[a,a,b,b,c,d,a,a] => [a,2,b,2,c,1,d,1,a,2]

def compressed(array)
	new_array = []
	counter = 0
	x = array[0]
	array.each{|c|
		if c == x 
			counter += 1
		else
			new_array.push(x, counter)
			counter = 1
			x = c
		end	}
	new_array.push(x, counter)	
	new_array
end

I'm glad my first whiteboard experience is behind me! I'm not sure how eager I am to jump into another one, but if I do, I feel confident in my ability to work through a problem and find a solution!
