---
layout: post
title:      "Scrooge Rails JS Portfolio Project"
date:       2019-02-28 15:52:35 +0000
permalink:  scrooge_rails_js_portfolio_project
---


This project is a refactoring of my Rails project, adding Javascript features to a selection of pages. 

The github repo can be found here: https://github.com/hengstrom25/js-scrooge

The requirements for the project presented several challenges, including combining Rails and Javascript on a view page, working with nested attributes, and reconfiguring routes so the app maintained the same functionality as it did when it was strictly Rails. 

I am hightlighting some of the requirements and how I chose to fulfiill them:

1. Must render at least one index page (index resource - 'list of things') via JavaScript and an Active Model Serialization JSON Backend.

- I chose to do this with the budget show page - one level deep into the user. The getBudgets function here uses a callback function to collect and render the list of Budgets. 

2. Must render at least one show page (show resource - 'one specific thing') via JavaScript and an Active Model Serialization JSON Backend.

- This is used in the Budget show page. Once again, a callback function is used to collect and render specific information about a particular budget. 

3. Your Rails application must reveal at least one `has-many` relationship through JSON that is then rendered to the page.

- Once again on the Budget show page, I added a button that, through Javascript, renders the list of transactions assigned to that budget. The button can then be used to hide the list. 

4. Must use your Rails application to render a form for creating a resource that is submitted dynamically through JavaScript.

- I reworked my edit form for a Budget to dynamically submit new information to update either the budget name or amount.

I look forward to continuing my studies in Javascript and working more on this app to fully integrate it into Javascript over time. 


