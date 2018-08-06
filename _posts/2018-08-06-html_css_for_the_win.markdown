---
layout: post
title:      "HTML + CSS for the win"
date:       2018-08-06 17:37:03 +0000
permalink:  html_css_for_the_win
---


In my last blog post, I said how much I was enjoying ORMs and Active Record. Today, I am making my way through the perils of HTML and CSS. The tasks and labs have really shown me how much I enjoy front-end development and what I refer to as the "finicky details." I love finding a missed /> or the wrong RGB color and watching the site transform in one simple fix. 

The code-alongs have been tricky mostly due to my attemps to view 2 screens at once and follow along. While I really enjoy most of these projects, I still find myself anxious to move foward and meet my stretch goals. I wish I could sit down and really enjoy these and not feel like I have to push push push ahead. 

The biggest thing I'm a little fuzzy on is Clearfix. From W3 Schools, I found the following:

If an element is taller than the element containing it, and it is floated, it will overflow outside of its container.

Then we can add overflow: auto; to the containing element to fix this problem:

.clearfix {
    overflow: auto;
}

The overflow:auto clearfix works well as long as you are able to keep control of your margins and padding (else you might see scrollbars). The new, modern clearfix hack however, is safer to use, and the following code is used for most webpages:

.clearfix::after {
    content: "";
    clear: both;
    display: table;
}

I think this will require some more practice on my part to really grasp how it works!

Until next time!
