---
layout: post
title:      "My Sinatra Portfolio Project"
date:       2020-10-20 03:08:17 -0400
permalink:  my_sinatra_portfolio_project
---


 The task for this project was to create a CRUD, MVC Sinatra application. We had to build a simple Content Management System (CMS) using the tools we had learned in Mod 2. 

I created a simple travel web application called ***Warda's Travel Diary*** that allows users to keep track of their vacations. My two models were a User and a Travel model, a user model *has many* travels and a travel model *belongs to* a user.  Users can login, logout, and signup. They can create, edit, view, and delete the trips they created; however they can only do this for their own vacations. A user can't edit or delete another user's vacation. There were a lot of steps involved in creating this project. Here are the steps:
	
Step 1: I used the Corneal Template Ruby gem to lay out my basic application structure. After that, I typed bundle install to load all my gems and dependencies. 

Step 2: I created two models: User and Travel that inherited from ActiveRecord. I establised *has many* and *belongs to* for my user and travel model.

Step 3: I created two tables, a user's and travels table using migrations. My user table had first name, last name, username, email and password. My travels table had trip name, itinerary, start date, end date, notes and user id. In order to migrate, I typed rake db:migrate in my terminal. I also created some seed data so I can use that data to play around with my application to make sure it's working.

I used Tux which is an interactive console to make sure my models were working. 

Step 5: I created files inside travel and user views folders. In the travel views folder, i created four erb files: index, new, show, edit.  I created 3 erb files inside users folder: login, signup, and show erb files. Inside the travel index erb, I iterated over a Travel.all array to view all the vacations inside that array. In the travel new erb file, there is a form that is displayed to the user to create a new vacation. The travel show erb displays one vacation based on ID in the url. The edit erb has a form used to update an existing vacation.

In the users folder, the login erb has a login form, the signup erb has a signup form and a show erb displays an individual users information.

Step 6: While I was creating the erb files, I was also working on creating my routes in the controller. I created three controllers, Application Controller which inherited from Sinatra Base and the other two controllers Travel Controller and User controller inherited from Application Controller. In config.ru I mounted those controllers. 

Step 7: I created helpers method to make sure that certain routes can only be viewed when the user is logged in. I also added flash messages to my application.

Overall, creating this project really helped me learn exactly how the routes are working and helped me gain a deeper understanding of how the Models, views, and controller are working together to create a working web application.





