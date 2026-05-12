---
layout: post
title: "Database Project - Second Client Meeting and Working Demo"
date: 2026-04-29 19:00:00 -0500
author: James Randle Jr
---

We just wrapped our second client meeting with Mr. Dan Turner from the Hendrix Advancement Office, and this one hit different. Instead of showing him slides and a mockup, we showed him actual working pages talking to an actual working database. That changes the entire feel of the conversation.

**How my role has evolved:**
In the first half of the project I was mostly playing PM and client liaison. By this second meeting that role had stretched into real coordination work: making sure Chris's front-end was talking to Jake's backend the way Dan would expect, prepping the demo script so we weren't fumbling around in front of the client, and translating Mr. Turner's reactions back into clear, actionable tasks for the team. Drew was right there with me on the coordination side, which made the prep way smoother than it would have been otherwise.

**What we showed Mr. Turner:**
- The homepage with the search bar, the intro sections, and a working "Possible Projects" table populated from the database
- The submission form for campus community members with the required fields (Name, Department, Project Description)
- An early admin interface for adding, editing, and removing projects
- The Hendrix orange styling pulled through the whole site so it visually belongs to the school

**What worked:**
- Watching Mr. Turner actually click around the site instead of just reading bullet points. That's the moment client meetings stop being theoretical.
- The schema held up under real data. The Donor, Opportunity, Proposal, Donation, and Review structure we mapped out in the first meeting did not need to be redesigned, which felt great to confirm.
- The user story format kept paying off. When Mr. Turner asked "can it do X?", I could pull up the exact user story we wrote weeks ago and either confirm it was done or flag it as upcoming.

**What did not work and lessons learned:**
- We were too cautious about the admin interface for this meeting. Dan made it clear that the admin side needs more polish and a real secure login, not just a placeholder.
- The donation flow needs better instructions. Right now a donor can land on a project page and not feel 100% clear on what to do next. The call-to-action needs more weight.
- Visual aids and graphics on the project detail pages are thin. Dan wants donors to feel something when they look at a project, not just read text.
- Demoing live to a client always exposes friction you didn't see in dev. Rehearsing the demo end-to-end the night before would have caught two or three small things before Mr. Turner saw them.

**Steps to complete by the final exam period:**
- Build out the updated admin interface with proper add, edit, delete, approve, and reject flows
- Implement the secure login using the 8-digit code approach we scoped
- Add stronger visuals and graphics to the project detail pages
- Write clearer instructions and a heavier call-to-action for the donation path
- Final pass on Hendrix orange styling and mobile responsiveness
- Final client review and handoff documentation so the Advancement Office (or a future team) can pick this up cleanly

**Connecting back to my PM internship:**
This entire second meeting felt like a small version of a sprint demo at Acxiom. Show the work, capture the client's reactions in real time, turn those reactions into a backlog for the next sprint. That loop is the actual job. Doing it on a school project with a real campus partner is the closest thing to professional product work I have done as a student, and I am grateful Dr. Goadrich structured the course this way.

**Looking forward:**
- Final implementation push with the team
- Final presentation to the class and to Mr. Turner
- A polished deliverable I can talk about in interviews when I am hunting analyst and PM roles in Memphis

We are close. The shape of the site is right, the schema is right, and the client likes the direction. The last stretch is about polish, trust, and finish.