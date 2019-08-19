---
layout: post
title:      "Model-View-Controller"
date:       2019-08-19 21:24:51 +0000
permalink:  model-view-controller
---


My rails projects have typically followed a design pattern called MVC, or Model-View-Controller. I'm often asked about it, and I wanted to take some time to study it further and solidify my understanding. 

The biggest strategy behind using MVC is that each section has a different purpose and the code is organized into these three parts to separate the different functions. 

Model - In my rails apps, the model is a Ruby class. It inherits from ActiveRecord::Base, meaning it inherits methods that work with the database. The model contains methods and logic related to the class that can be used throughout the application.

Controller - The controller connects the models, views, and routes. Methods are defined that take the user's input and decide what to do with it. It's the main "brain" of the application. 

Views - The views are what the user interacts with. They do not contain much logic and should only render what is received from the database. 

The follow diagram shows the path of an MVC application:

![](https://images4-e.ravelrycache.com/uploads/operadiva25/643274326/mvc_medium2.jpg)

A user will click on something on your app, such as an "add" button. That request is sent to the controller, which processes it and requests the information from the Model. The model sends it back to the controller, which then relays the information to the view. The view is what is sent back to the user's browser and the process begins again. 

I look forward to continuing my process of finding topics to learn more about !
