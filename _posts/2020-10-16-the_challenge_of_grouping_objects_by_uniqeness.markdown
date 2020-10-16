---
layout: post
title:      "The challenge of grouping objects by uniqeness"
date:       2020-10-16 01:16:25 -0400
permalink:  the_challenge_of_grouping_objects_by_uniqeness
---

    As part of my coding challenge for my rails assessment I was told to change my static home page for my profile, which has a list of tattoo artists that a user could choose from, to a dynamic list of artists who were previously submitted to the database by the user. This a whole lot of duplicates which I needed to get rid of. First I shoveled in every artist object into an array and called the #uniq method on it. Then while looking at the result I remembered something. All objects are by default unique! Even if the name atribute is the same the ID is different which makes it unique. The way I solved this problem was the a method that is reliable when it comes to problems that involve uniqeness-a good ol'e fashion hash. The keys of hashes ,just like objects, are unique by default. First I made an empty hash, then iterated through each artist and set each artist's name, which is the artist's attribute, as a key and set that value to the artist object itself. The reason this worked is because a key of a hash will reassign its value when another duplicate key is compared with it. I then iterated through the hash and displayed each name as a clickable link to the artist path for the user to view. 
