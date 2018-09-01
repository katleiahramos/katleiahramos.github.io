---
layout: post
title:      "Rails + JQuery Project: Project Management App 2.0 "
date:       2018-09-01 19:25:10 +0000
permalink:  rails_jquery_project_project_management_app_2_0
---


I previously had made a [Rails app](http://katleiahcodes.com/rails_project_project_management_app) that was inspired by a PhD student doing research in their lab. The app was created to help them manage long term projects by breaking each project into tasks and assigning those tasks to group members. 

My original Rails App used conventions of RESTful routing and rendered information statically on a web page. 

After learning JQuery and Ajax, I knew how I could migrate the project management app toward a dynamic, single-page application. I was going to use my knowledge of JSON, APIs, and JQuery/AJAX to dynamically add content to the web user interface. 

This project was particulalry exciting because I was building on code that already existing, and could really focus on the user-facing functionality of my project. 

Once I had my general idea, I reached my first point of struggle: Where do I start?? 

My Workflow 

**User Story Brainstorm **

The first thing I decided to do was sit down and write out some user stories. I went through the [requirements listed](https://github.com/learn-co-students/rails-js-assessment-v-000) and started to write down a user story to go with each to form my MVP. 

Other ideas that came to mind while doing this I put in a seperate list called "additional features". 

Previous I might have something like:
> User can create a task 

Now that I wanted to make it dynamic in the DOM it became:

> User can create a new task and it will be added to the DOM without a refresh 



**Move through user stories one-by-one **

Now that I had a list of user stories, I decided to attack them one-by-one. 

building from the example above, in order to create a task I needed to render a form. I would need to use JQuery to listen fo the "submit" event 

```
  $('.taskForm').on('submit', function(event){
    event.preventDefault();
		const url = this.action
    const values = $(this).serialize();
  })

```

and then use AJAX to handle the route 

```
$.post(url, values)
```


and once that was created successfully, get a JSON back to work with and append to the DOM. 

```
$.post(url, values).success(function(response){

      const name = response.name;
      const projectId = response.project.id
      const taskId = response.id
			
			// generate HTML that will append task as a button 
			const button = buttonizeTask(name, taskId);
			
			//add the new task button to the project div it belongs to 
			 $(`#project-${projectId}`).find(".tasks").append(button);
```


Using the [JS debugger](https://developers.google.com/web/tools/chrome-devtools/javascript/) came in EXTREMELY handy for checking my variable values and making sure my event handlers were hitting the right functions. 


After working on through the user stories (which took some time by the way) I was ready to move toward wrapping up. 

**Check basics **

While I had added a lot to my new single-page application, I wanted to make sure my app still had all of it's CRUD functionality that it started with. Could a user create, read, update, and destroy a task? a project? 

I also made sure that my forms had validations to ensure good data persisted into my database. I made sure there was user authentication on my pages, so users must be logged in to view projects. 


**Test! **

The last step I made sure to do was to have people test out the application to see what else I could change, or give me ideas for future features.  



**What I learned**
After completing this project, I felt extremely proud of the final product. The project helped solidify main technologies and uses of JS, JQuery, and AJAX. More importantly, while completing this project I got a ton of ideas for future projects where I could utilize these technologies. 
