---
title: Week 2
date: "2019-03-29T22:12:03.284Z"
---

The second week of Lambda Labs started out with more planning; this time we were tasked with planning in detail what we would need to do for the entire week. To reach the week's milestone's we'd need to have 80% of our APIs completed on the back end, 80% of the data consumable on the front end, and integrated third-party APIs (in my team's case, Auth0 and Stripe).

## Summarize the work you did over the course of this sprint, including the challenges you faced, the tools you used, and your accomplishment

On Monday of this week my team and I spent the entire day working on our plan for the week. At the end of the day we met with our Section Lead to present our plan. I led the presentation this time around.

On Tuesday, Wednesday, and Thursday, I primarily focused on writing the queries and mutations on the back end for each of our project's data types. This was a bit of a challenge at first as my experience with GraphQL prior to Labs was pretty minimal and I had no experience writing mutations for data that had relationships to other data. I struggled at first writing mutations for workouts, for instance, because workouts are linked to a specific schedule ID. Once I figured out how to use the connect feature and the context object it was smooth sailing and I was able to write the back end queries and mutations for several of our types.

## Pick one of your tickets and provide a detailed analysis of the work you did

https://github.com/labs11-workout/labs11-workout-BE/pull/29

This ticket is a bug fix I completed Thursday morning in response to an issue that occurred when one of my teammates tried to query Saved Workouts on the front end. It turns out that I had originally connected the "user" field on Saved Workouts to a userId that was being passed in as an argument in the query. Instead, the userId should have been attached to the context object so that the userId of the currently authenticated user will be connected to the user field on Saved Workouts. That way the query will dynamically return the saved workouts for the authenticated user.

## Reflect on your experiences forming a team. 
### What did you do to help the team solidify as a group? What did you do that you now realize caused friction in this process? What are you doing personally to make sure that everyone on the team, including you, has  a voice in decision making?

I think my team as a whole has done a great job of forming a cohesive unit and making sure that everyone's voice is heard. We spend nearly the entire day each day in a Zoom meeting so that it's easy to ask questions, raise concerns, or update each other on the status of our work (when we've completed a feature, made a pull request, need a review, etc.). Doing things this way allows everyone to be aware of everything that's going on and ensures that we can always speak up about questions/issues in real time. 

If there were one thing I might suggest we (or I) do differently, it's communicating more about the "nuts and bolts" of our individual work. We've had a few instances where we've discovered bugs or issues later on that, in retrospect, seem obvious and probably could've been caught before the code was merged if we'd all double-checked with each other.
