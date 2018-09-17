---
layout: post
title:      "Sinatra Portfolio Project: Beer Enthusiast"
date:       2018-09-17 11:54:29 -0400
permalink:  sinatra_-_beer_enthusiast
---

I am pleased to have finished the main framework for my Sinatra Portfolio Project. I found this project much easier than the CLI Data Gem Project in many ways, the main reason being that I was more comfortable using a local environment and was able to build the entire project correctly the first time. 

This project required some planning and work before the programming really began. Setting up the file structure relied on having a plan for how the program would work, since I needed to decide what the different models and controllers would be. Once I had that planned out, I was able to set up the main files needed and being setting up the migrations. 

I've done migrations many times now in this program, but there was something amazingly satisfying about setting up a file from scratch, running rake db:migrate, and seeing it work. There have been many times during this process when I think there is no way I could ever get a "real' thing to work and when it does, I feel like I've won the lottery. 

Setting up the models and application contoller was pretty straight forward, as well as the UserController. 

What began to really trip me up was the sessions. A rogue "s" gave me hours of errors and filled my tables with broken information. Once I was finally able to fix the mistake and clear the tables so I was working with fresh information, progress continued.  It was rather fun to realize I could use SQL to see what the problems were, both at this moment and later on. I love when learning comes full circle. 

Adding in the third level of "Reviews" was more complicated than I expected. Because I have everything set up to relate to specific beers and users, the associates were complex and made for a lot of trial and error. A few pages had me really stumped for many hours, but I learned a lot about how to check what was actually happening to give me clues to figure out how to solve the problem. 

All in all, this was a big learning experience and I am pleased with the results. I had to put aside some of my design tendencies in the interest of just getting the program to work, but I look forward to playing with the styles so I can make not only a functional app, but a fun, useful one.
