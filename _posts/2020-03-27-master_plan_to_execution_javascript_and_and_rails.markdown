---
layout: post
title:      "Master Plan to Execution: Javascript && Rails"
date:       2020-03-27 22:25:34 +0000
permalink:  master_plan_to_execution_javascript_and_and_rails
---


All great projects begin with a great plan.

Before starting this project, I wanted to make sure I had an plan for how I wanted it to look and the functionality I want it to have.

This was a very exciting challenge. This was our first project adding Javascript. And we weren't allowed to use any frameworks. So, vanilla JS it is.

## The Process

After going through this roller coaster and talking to other people in my cohort this seemed to be the general process of creating this project.

**1. ok cool
2. OMG (The Wall)
3. Calm a little
4. Get Back to Work
5. ok. I'm just going to turn in something**

What was my something?

I created a web application called BookTap. The concept is to have all your books on tap and add comments related to the book. Plenty of times, I come back to a book I've read. But, I don't remember any exact quotes or thoughts I had while reading the book. So, I created something I would use as my web application.

After the idea phase, I had to start building.

I decided to use Postgres instead of the out of the box sqlite3 that comes with creating a new rails project. This was to help with future functionality I wanted to add and hosting.

I kept track of the commands I ran, because they aren't stored anywhere. You just see the product of the commands. So, to create the Rails backend with a Postgres database. 

My database schema was simple for this project. 

Then, I went on to add the coordinating Models and Controllers. I didn't need Views, because Javascript would take that place.

I also added serializers for Json to determine exactly what information I wanted to pass through. For example, I didn't need to pass through the created_at and updated_at timestamp columns from my database.

## Javascript
With my backend created and configured for my project, I could begin to work on the Javascript. I went through four phases of the javascript section

1. Get everything to work
2. Get things to look decent
3. Get things to look decent and work
4. Refactor


As you can image #1 took the longest amount of time. I only had one file index.js and I had to get everything to work in there.

One very helpful piece, while trying to make things work was testing and testing in small chunks.

console.log() was my friend when it came to testing my fetch requests to my Rails API.

One thing I didn't know before I started this javascript project was that I would have to create DOM elements each time the page loads to render the data from my fetch request.

I created a comment button, for users to add comments to their favorite books. There are many pieces of code that allow that comment button to work. To simplify it I have:

1. An event listener for the button
2. A function to create a form that allows the user to create a comment
3. A function to create actually create the comment and save it in the database sending a POST request through fetch
4. Displaying the new comment on the DOM for the user to see

There are a lot of moving parts to this project. And both creating and debugging felt surgical.

I hit the wall and got stuck plenty of times during this project, especially on the short deadline.

I learned the only way to get over the wall is by getting help, whether that's someone pushing or lifting hands to pull me over the wall that's how I got over it. I'm thankful to my Flatiron cohort and instructor for helping me to this point.
