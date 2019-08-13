---
layout: post
title:      "Active Record Associations"
date:       2019-08-13 20:41:14 +0000
permalink:  active_record_associations
---


One of the great things about job interviews is that they help you identify pieces of your knowledge that you may need to brush up on. (And it's a good idea to think of this as a positive! Everything is a learning experience!) In my experience, it's not always a make or break if you don't know the answer, but it's always a good idea to refresh your memory if something was a little fuzzy. 

One of the topics that came up in a recent interview was active record associations. The app I generally talk about utilizes 2 of these associations, but I found myself struggling to remember the rest. 

There are six types of active record associations in Rails:

belongs_to
has_one
has_many
has_many :through
has_one :through
has_and_belongs_to_many

These associates are included in your models as part of your model-view-controller. 

For example:

class Category < ActiveRecord::Base
        has_many :recipes
end

Let's break that down line by line. 

On line 1, we're defining the Category class, which is inheriting from ActiveRecord::base. That means it's inheriting the built in methods that come with Active Record. 

On line 2, we're saying that a category has many recipes (which, in turn, probably means that a recipe belongs_to a category). *The colon in front of the recipe marks it as an argument to the method. So, it would also be possible to write it as has_many(recipes).* This specifies a one-to-many association and helps us streamline our code. 

I look forward to continuing to brush up on my Active Record and Ruby methods and learning even more along the way!



