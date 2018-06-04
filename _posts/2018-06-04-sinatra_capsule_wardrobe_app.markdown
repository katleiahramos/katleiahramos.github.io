---
layout: post
title:      "Sinatra Capsule Wardrobe App "
date:       2018-06-04 17:31:38 -0400
permalink:  sinatra_capsule_wardrobe_app
---


## The Context 

You might be wondering, what is a capsule wardrobe? 

Via Wikipedia it is the following 

> Capsule wardrobe is a term coined by Susie Faux, the owner of a London boutique called "Wardrobe" in the 1970s. According to Faux, a capsule wardrobe is a collection of a few essential items of clothing that don't go out of fashion, such as skirts, trousers, and coats, which can then be augmented with seasonal pieces.
> 

Capsule wardrobe is often synonymous with a minimalist wardrobe or parallel to a minimalist closet. 

What is a minimalist wardrobe? Pretty much what it sounds like. Cutting down your closet into a few essential pieces that you really love (your capsule). Your capsule can serve multiple purposes such as:
* Defining your style or your brand. 
* Saving you money by helping you keep track of what you really need and what you really DON'T need (if you're like me and have something like 10 black shirts...) 
* Promoting sustainability in the world of fashion, where so much consumerism revovles around the idea of "fast-fashion" (cheap & quick), which can lead to non-ethical production of clothing. 



## The Process

**1. 5 minute brainstorm **

The first thing I did was sit down, set a timer for 5 minutes, and brainstorm ideas. I didn't add detaisl, I just wanted to get out as many ideas as possible so that I could choose and move on. I came up with a couple, but there were two that really stuck out to me. One was to create a teacher portal, with models like teacher, student, class. The other was to create a wardrobe capsule with models like user, clothing, and capsule. I ended up choosing the capsule app. 

The reason I feel this step was important to me personally was that with my CLI app, I would get these ideas part of the way through of different directions to go with my project, or ditch my idea and go a different way entirely. 

I think it's in good practice to make a decision and commit to it. No one says you can't go back and create more sinatra projects later!


**2. Wireframing! **

I had attended a sinatra lecture earlier in the week to prepare. I'm so happy I did because the instructor (Howard) pointed out that planning and wireframing were crucial first steps in starting the project. 

I did my planning a couple of different ways. First, I created a diagram of my model associations so I could keep track of the has_many,  belongs_to, and the has_many_through relationships. I created the diagram below using draw.io

(https://imgur.com/a/cOuGW8h)

After that I wrote out the attributes for each model, making sure that if there were any belongs_to relationships that the model included a foreign key in their table. (for example, pieces needed to have a column named user_id since a piece of clothing belongs to a user.) 

After I looked over my attributes and model associations, I was ready to write the migrations and model files!

**3. Writing the models and associations **
 
 I can't stress enough how easy this step was because of the previous step. Planning is something I've really learned to love and use A LOT. I feel like planning ahead allows me to really understand what I'm doing and also saves me a ton of time. 
 
**4. Testing with Tux **

WOOO, testing with tux. Tux is a fantastic Ruby Gem that allows you to work with your relationships and database in a test space.  Before I went on to write any more code, I wanted to make sure that all the assocations (has_many, belongs_to) worked the way I was expecting them to. This is also key to understanding how your app is going to work and reducing issues moving forward. 

**5. Building the routes, step-by-step**

Now was time for a lot of coding. The process I used was to image how the user was going to use the sinatra app, from beginning to finish. The first step would be to sign up, so that was the first route I created. I started in my controller, wrote the route, and threw in a pry to make sure it was working. Spun up shotgun, tested, it worked, moved on. Next step I created my view file, threw a pry in there, made sure it was my route was working, then wrote code. 

Writing the code for my controller essentially went along in this pattern, testing along the way that everything was doing what I was expecting it to do. 


**6. Refactoring/cleaning it up **

There were many times during the process in step 5 that I wasn't sure if I was going to need a certain view (for example, I originally had a view of all the pieces, but later decided to just show all pieces on the user show page). During step 5, I just wrote the code. It's almost felt like a free-write. I knew I could always go back later and refactor it. 

This step was a little tricky. After everything is working, it's hard to want to change anything in fear that it will break everything. The great news is, if it breaks, there will be a solution, and I feel that the idea of making code work, then breaking it, then fixing it again, is just the process of problem-solving and coding overall. Art is never finished, and sometimes you have to break it a little bit to help the product be at it's best. 


**7. Done! **

The great thing about refactoring my code was that I was able to look at the finished product with a true understanding of my application from backend to front-end. Finish the project was a great accomplishment, espeically to see my idea transform from paper to a real sinatra web app. 
