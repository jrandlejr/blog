---
layout: post
title: "Lab 8 - ASP.NET Razor Pages: My Favorite Music Albums"
date: 2026-03-10 10:00:00 -0600
author: James Randle Jr
---

In Lab 8, we built an interactive web application using ASP.NET Razor Pages that connects to a real SQLite database with full CRUD functionality.

### The Tutorial (Step 1)

The easiest parts of the tutorial were the early steps like setting up the project and understanding the file structure. It felt familiar coming from Jekyll because both frameworks have a specific way they want you to organize your files. The Razor Pages structure with the Pages folder and the .cshtml files reminded me a lot of how Jekyll uses layouts and includes.

The confusing parts were definitely the database side of things. Entity Framework Core and migrations were completely new to me. The concept of running dotnet ef migrations add and dotnet ef database update to essentially version control your database schema took a while to wrap my head around. Also Part 7 where we added the Rating field gave me some trouble because I had to make sure my terminal was pointed at the right directory before running dotnet build, which caused an MSB1003 error at first.

### Building My Own App (Step 2)

For my own application I chose to build a Favorite Music Albums tracker because music is something I genuinely love. I used the same concepts from the tutorial but applied them to an Album model with fields for Title, Artist, Year, and Genre.

The most difficult part was that the scaffolding tool kept failing when I tried to auto generate my pages. I kept getting errors related to the DbContext not being resolvable, even after adding a design time factory. Because of this I had to manually create all five pages, Index, Create, Edit, Details, and Delete, by referencing the tutorial code and adapting it for my Album model instead of the Movie model. It was actually really helpful because I had to understand what each file was doing instead of just letting the tool generate everything automatically.

I also ran into a build error with my Edit.cshtml.cs file that took a while to track down. The file had some kind of hidden encoding issue and the only fix was to delete it completely and recreate it from scratch, which then resolved everything.

On top of that I had to manually add the Albums link to the navigation bar by editing the shared layout file, and I cleaned up the table styling on the Index page by adding Bootstrap table classes since the default presentation had all the text crammed together.

### Screenshots


![My Alt Text]({{ '/assets/images/MusicDataBase.png' | relative_url }})




### Jekyll vs Razor

Both Jekyll and Razor are frameworks that give you a structure to follow, but they serve very different purposes. Jekyll is great for static content like blog posts where the data does not change. Razor is built for dynamic applications where users can create, edit, and delete data in real time through a database. Jekyll feels simpler because you are mostly just writing Markdown and HTML. Razor requires you to think about models, database contexts, migrations, and page models all at once. That said, once everything is connected it is really powerful.

### Confidence Level

I feel more confident than I expected after finishing this lab. The errors I ran into actually helped me understand the framework better because I had to dig into what was going wrong instead of just following steps blindly. I think I could build another Razor application on a different topic without too much trouble, though I would definitely still reference the tutorial and my notes along the way.

You can find my Music Albums repository here: [jrandlejr/lab8-ASP.NET-Razor-Pages](https://github.com/jrandlejr/lab8-ASP.NET-Razor-Pages)