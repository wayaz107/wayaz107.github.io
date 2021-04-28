---
layout: post
title:      "React/Redux Project"
date:       2021-04-28 06:47:45 -0400
permalink:  react_redux_project
---


For my final project at Flatiron School,  I decided to do my app on skincare products. Users can create, view and delete products. 

The project requirements were to use React and Redux for the front-end. For the back-end, we had to use Rails as an API to handle our data. 

**SETUP**

I started my front-end project by using 'create-react-app' command in terminal. This auto-generated the basic layout, including App.js and index.js as well as some other files.  

To start my back-end, I used the command 'rails_new_my_project_api'. The '-api' flag allows rails to create all the files needed for rails app, except for the view folder because our React front-end will be handing all the views. I used rails generator to create models, controller, and database. 

**LAYOUT**

We were required to use five stateless components. The stateful components have state and are keeping track of changing data, while stateless components print out what is given them via props. We also had to use Redux to handle our state. Redux makes use of the store, which holds the whole state tree. The only way to make changes to the store state is through actions. Redux Thunk is a middleware used to allow for dispatching actions asynchronously. 

**CONCLUSION**

Overall, this project was challenging. I am proud to have finished building this project and hope to continue growing  in this coding field and expand this project further.
