---
layout: post
title:      "My CLI Weather project"
date:       2020-08-02 18:47:52 +0000
permalink:  my_cli_weather_project
---


   I decided to make a weather CLI for my first Flat Iron project. I decided to use the 'HTTParty' Gem for my API.  ‘HTTParty’ allows us to send the GET request, retrieve XML object and format it into nested arrays. I found using an API was more simple than scraping a webpage for its data. I used the website http://api.openweathermap.org to get an API key for the current weather for worldwide cities. I saved the response I recieved from HTTParty, which was a hash of hashes, and iterated over it to select the attributes of weather I wanted. 
	 
	 An interesting challenge I had to solve was how to implement control flow for whether the response I received was valid or not. There are several methods for accomplishing this. I could have wrote a condition that if the response I receieved did not returned certain errors then to store the desired data. I decided to write a condition saying that if the response I recieved did not have a key "message" then it was valid. This was because there would be a key with a 'reponse' string whenever there would be an error. I then created a new instance of city with the selected part of the hash I wanted to display. Every city instance was initialized using the #send method. Instead of setting each of the City's keys to their values line by line I used the #send method. This interpolates the keys to equal their given value for every key of the city. This is far preferable then writing out each city's key and setting them to their respective values which would take up unnessecary space. 
	 
	 In this CLI project I learned about saving objects in order to make your code run faster. I used the find method to see if the user had previously searched for the city they had entered. If they have, then that city object would be stored in a City class variable. This saves time by nit having ti make another request from the API which would take unnecessary time to load since the API already made a request for this city that the user previously entered. 
	  
