---
layout: post
title:      "React-Redux Project: Bark Park - Lessons Learned & Helpful Tips "
date:       2018-10-15 16:42:17 +0000
permalink:  react-redux_project_bark_park_-_lessons_learned_and_helpful_tips
---


**The Context**

Going into my React-Redux project, I knew I wanted to create a one-page CRUD (Create, Read, Update, Delete) application. As I usually do, I went to my friends/family for ideas. 

My friend Curtis just adopted two dogs. The dogs have a lot of playful energy, so he's a regular at his local dog park. When I told Curtis about my project, he threw out an awesome idea - a dog park (social) app where you can see when other dogs are at the park, how busy the park is, and check-in to that park so others can see you and your dog are there. 

I loved this idea because I have two dogs myself (see picture below), and I've met a lot of cool people at dog parks and my dogs have met a lot of cool dogs at the dog park - dogs should be able to meet up with their friends too! 


![My two dogs sleeping on the couch](https://i.imgur.com/qfFG0UK.jpg)


Below are some lessons learned and tips to think about when going into building your final project! 



**The Workflow**

After my JQuery Project I got really into using [Trello](https://trello.com). Trello is a great application for keeping track of team projects and tasks. In fact, my last project, [Project-Management-App](http://katleiahcodes.com/rails_jquery_project_project_management_app_2_0) , was inspired by it. 

I also recently got into watching Silicon Valley, and there is an episode where """Jared""" (real name Donald) introduces SCRUM to the Pied Piper team. 

<iframe src="https://giphy.com/embed/xT1XGOGdyDrL2BTfxK" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/siliconvalleyhbo-xT1XGOGdyDrL2BTfxK">via GIPHY</a></p>


I got curious and google-researched more about [SCRUM](https://searchsoftwarequality.techtarget.com/definition/Scrum). I figured creating this project board could simulate a [SCRUM board](https://www.quora.com/What-is-scrum-board). 


Essentially, what the project board represents is a structured "to-do" list form of user stories. 

If you want to see what my project boards looked like you can click [HERE](https://imgur.com/eH8xkM3). 


**Rails** 

Here's the thing. I didn't start with the rails part of my application first, but I wish I had. I started by creating my React application, connecting it to a store via Redux, and getting the whole front-end working. So why start with the Rails side you ask? In retrospect, I think it could save someone a lot of time. 

> So why start with the Rails side you ask? In retrospect, I think it could save someone a lot of time. 
> 

Back in the rails app days, you have an MVC framework - Models, Views, Controllers. In many ways I see the React (which is a front-end library) as a replacement to the V - views. The front-end of the app should have little data maniuplation, and should be responsible for displaying the data on the user-facing (or client-facing) side. This is why when completing a Rails app, I wouldn't start with building out the views first. I would start with creating my models and structuring my database, then testing that my back-end behaves the way I expect it to. 

I created my React front-end first. I got everything working with the store (I could create, read, update, and delete), awesome! Once I started hooking it up my rails api, I realized there was a lot of code I had written that was no longer needed. 

> Once I started hooking it up my rails api, I realized there was a lot of code I had written that was no longer needed. 


If I could go back, I could have saved myself a lot of time by just creating my Rails side, building out models/DB, and creating the controllers to just send my React front-end the data it needed instead of manipulating data (that wouldn't end up being stored) on the front-end. 

**Wireframing**

WIREFRAMING. is. so. important. Specifically for React, it's helpful to plan out containers and components. 

Here is a wireframe draft of my application. 

![](https://i.imgur.com/1jMhg2V.png)

By creating this wire-frame I could plan out my containers and components. 

*Containers *

The page has two main sections: Parks and Map. From that I knew I would need two containers, ParksContainers.js and MapContainer.js. These two containers would live in my App.js component which embodied the whole page. 

*Components*

Looking at the each container I could see the different components that each contained. 

Parks Container: Parks (the visual component that displayed the parks) and ParkCard (the visual component that displayed each individual park). 

Map Container: this container only had one thing - the map. 

Wireframing can also be really helpful when creating the design for your User Interface. Instead of spending a lot of time going back and fourth between layouts, box sizes, where buttons should go (I spent way too much time doing all these things before I finally realized I should do some wireframing), you can just focus on building your existing design with little decision making. 



**The summary **

This project taught me a lot of things: how to integrate with the Google Maps API, how to connect a React-Redux front end with a Ruby-on-Rails AP, and how to organize a workflow for React project. My favorite things about this project is that there is still so much that can be built! I look forward to adding more features and expanding the project further. 




















