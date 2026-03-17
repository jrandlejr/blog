---
layout: post
title: "Lab 9 - Entity Framework: Stash University"
date: 2026-03-17 10:00:00 -0600
author: James Randle Jr
---

In Lab 9, we expanded on our understanding of ASP.NET Razor Pages by integrating Entity Framework Core with multiple related tables, complex queries, and concurrency management. The project was built around a university management system I called Stash University.

### The Tutorial (Step 1)

The easiest parts of the tutorial were the early steps of setting up the project and scaffolding the Student pages. Coming off of Lab 8, the Razor Pages structure felt familiar and I was able to move through Parts 1 and 2 quickly. The sort, filter, and paging section in Part 3 was also satisfying once it clicked because you could see the results immediately in the browser.

The confusing parts were the migrations. Every time the tutorial had me update a model I had to make sure the migration was run before the app would work again. There were a few moments where the connection string kept reverting from SQLite back to SQL Server because the tutorial is written assuming SQL Server by default. Catching that pattern early saved a lot of headaches later on.

Part 5 was the most involved section of the whole tutorial. Adding multiple related entities like Instructor, Department, Course, OfficeAssignment, and Enrollment all at once meant that one missing using statement or a wrong namespace could cause a chain of build errors across multiple files. I had to work through several of those carefully before getting a clean build.

### Working with Multiple Tables (Step 2)

Working with multiple related tables was significantly more complex than the single table in Lab 8. In Lab 8, the model was self contained and changes only affected one file at a time. In Lab 9, a change to one model could ripple through the DbContext, the seed data, the scaffolded pages, and the migrations all at once. For example, adding the Age field to the Student entity meant updating the model, the seed data in DbInitializer, the Create and Edit page models, the Razor view files, and the sort logic in the Index page.

The concurrency section in Part 8 was also a new concept entirely. The idea that two users could load the same page at the same time and unknowingly overwrite each other's changes is something I had never thought about before. Seeing how EF Core handles that with concurrency tokens made the real world complexity of database applications much clearer.

### My Modifications

Beyond the base tutorial I made four changes to push my understanding further. I renamed the application to "Stash University" throughout the layout and homepage. I added an Age field to the Student entity and carried it through the model, seed data, migrations, and all five Student pages. I added I for Incomplete and W for Withdrawn to the Grade enum to reflect how real university grading systems work. Finally I added Age as a sortable column on the Student Index page alongside Last Name and Enrollment Date.

### Confidence Level

I feel more prepared for the final project than I expected after finishing this lab. Working through a multi table database with real relationships between entities gave me a much better picture of what building a real application looks like as we dive into working with different communities across Conway, Arkansas. 

You can find my Stash University repository here: [jrandlejr/csci340lab9](https://github.com/jrandlejr/csci340lab9)