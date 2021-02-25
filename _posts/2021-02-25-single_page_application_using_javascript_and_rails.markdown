---
layout: post
title:      "Single Page Application using JavaScript and Rails "
date:       2021-02-25 06:16:55 +0000
permalink:  single_page_application_using_javascript_and_rails
---


The requirement for our fourth project was to create a web application that used a Ruby on rails as a backend and the front end with JavaScript. We had to bring Ruby and JavaScript together into one single app.

The basic setup for the project was to create two separate repositories. We went through all the usual steps for creating the app’s elements:

Backend (Ruby on Rails):

* Create models and relationships

* Create the database tables and seed

* Create controllers 

* Create routes

* Run Rails s for starting the server (this would open it by default on    
  http://localhost:3000)
	
	
Frontend(JavaScript):

* Create index.html

* Create index.js

* Create adapter files to handle fetch calls

* Create model class files


The frontend creates functions that create and append elements. We are using JavaScript to render our views. Previously in the Rails project, we had view files that helped render our views but in this project, we use JavaScript frontend for that. The Rails backend is used to create the APIs needed for JavaScript to fetch data for CRUD. 

In order to send data from backend to frontend, we had to render our variables in controller with render json. For example:

def index
    @lists = List.all
  	render json: @lists
end 
	
This means that we can now go to* http://localhost:3000/lists* in our browser and see the data in json format, which can be now easily fetched with JavaScript.


These are just basic steps to getting started with a single page application. I build my project about list of activities you can do in different seasons in Chicago. Users can view the list depending on the season selected and also can add more activities. This was a very challenging project but completing it helped me deepened my understanding of JavaScript. 
	


