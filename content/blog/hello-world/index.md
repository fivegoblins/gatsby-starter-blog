---
title: Week 1
date: "2019-03-22T22:40:32.169Z"
---

The first week of Labs was devoted mostly to planning. It was hard not to jump straight into coding on day one but, looking back, I'm glad we took as much time as we did to design the Product Canvas and plan out everything we would need. 

I've been asked to answer a few questions about what I did during week 1, so here goes:

## Summarize the work you did over the course of this sprint, including the challenges you faced, the tools you used, and your accomplishment


This week was different than I imagine the next four weeks of Labs will be in that, while each of us on the team contributed individual PRs, we did all of our work in a team-wide zoom meeting and so all of us contributed in some way to each other’s work. My individual contributions in terms of PRs include building out the Prisma data model. I had some experience with GraphQL and Prisma in the past and so felt that I was up to the task of modeling out the relationships for each data type our project needed. I got the data model 90% there and then we as a group made a few extra alterations while we were seeding the test data. Additionally I think I added value to the team, helping out others in the team-wide zooms by answering questions and providing suggestions as they wrote their code.


## Pick one of your tickets and provide a detailed analysis of the work you did.

https://github.com/labs11-workout/labs11-workout-BE/pull/4/files 

This was my first PR on the project. I started building out the Prisma data model in this ticket. When generating a Prisma server, the datamodel file comes preset with a Users type that contains fields for a unique ID and a name. We as a team were still hammering out details of what our user model would look like so I left that alone for the time being and moved on to other data. I modeled out a Schedule, which has fields for a unique ID, a time of type DateTime, and a related User. I made all of these fields not-nullable. I created a data type called SavedWorkout which will represent reusable workouts that premium users make and save that are not related to any particular schedule. For the time being I only gave that type a field of unique ID. I also created the Workout data type, which has a unique ID, a name of type String, and a related Schedule. All of the fields here are also not-nullable.


## Reflect on your individual contributions to analyzing the project specification and writing the TDD. 
### Describe the research you personally conducted to find out information on a competitor, investigate a technical solution to a specific problem, or define your customers.

I contributed valuable insight to analyzing the project specifications and writing the Product Canvas because I have firsthand experience as a user of similar products to the one we’re trying to build. I signed up for the Workout Tracker team because I’ve used several different fitness tracking apps in the past and been dissatisfied with all of them. One of the problems with competitors that I identified, and that my teammates agreed we should try to fix in our app, is that many fitness apps ask users to provide a huge amount of information up front in order to make an account. 

It can be overwhelming and discouraging to users to have to input a ton of physical and personal information simply in order to sign up for an app, so with my insight we agreed that this information should be optional and completely up to the user whether they want to make use of the ‘progress-tracking’ aspect of the app. 

Additionally I’ve found that other products either focus entirely on weight loss and tracking calories burned vs. calories consumed (ex. myFitnessPal), or they are highly specialized to athletes and focus entirely on sports performance (ex. Training Peaks). I think that my knowledge and research contributed to the team’s decision to make this app do either of those things, depending on what the user wants. It can be just a simple workout log, it can be a progress tracker that shows you how much weight you’ve lost and how your measurements have changed, or it can be a training journal that allows you to visualize how your athletic performance has changed over time. 

In this way we’ve expanded the demographic that our product appeals to: we can attract beginners who are looking to schedule workouts to keep them accountable,more serious lifters who are interested in aesthetic goals, and fitness fanatics who are trying to reach peak athletic performance.

