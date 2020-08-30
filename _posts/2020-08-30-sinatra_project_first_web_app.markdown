---
layout: post
title:      "Sinatra Project. First web app"
date:       2020-08-30 21:51:54 +0000
permalink:  sinatra_project_first_web_app
---


   I consider this project to be a serious accomploshment and milestone for my coding journey. This is my first web application I have ever built. My application is called virtual garage. On my application a user can create a profile and store representations of their tools along with the quantity of their tools. My tools model validates presence of a tool's name along with a tool's quantity. The users model validates uniqeness of username and it has a secure password. many of these methods come firom sinatra macros which writes these methods for me. The tools and users models are connected with a belongs to-has many relationship. With Active Record all I had to write was the lineds belongs_to and has_many in my models. Active record writes the sequel needed to connect these two models, however I neded to wtire the tables for them myself. It was very intersting to have to protect againt url hacking for this project. All I had to do was insure the user could only navigate to the edit page if the tool of the edit page belonged to that user. I wrote a helper method to redirect the user back to the login page if they tried to access a tools page without being logged in. I then just added that code to all of my tools controller methods. I used flash messages to inform the user why the attempt to see different pages was blocked. I eventaully want to get into cyber security so protecting agaist url hacking was especially interesting for me because this would be my first real experience in writing code to insure security.
