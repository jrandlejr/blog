---
layout: post
title: "Database Project - First Client Meeting, User Stories, and Mockup Reflection"
date: 2026-04-08 19:00:00 -0500
author: James Randle Jr
---

For our Database & Web Systems final project, my team and I were paired with the Hendrix Advancement Office. Our client, Mr. Dan Turner (Director of Advancement Service), wants us to build a standalone website that showcases funding opportunities at Hendrix. The site needs to act as a curated list that the advancement staff can pull up when they're working with prospective donors, covering named spaces, equipment purchases, faculty and academic projects, and student experience initiatives.

This first stretch of the project has been all about turning what the client said in the room into something the team can actually build.

**My role so far:**
- Lead point of contact with Mr. Turner during and after the first client meeting
- Pulled the user stories together for three different user types: advancement staff, donors, and campus community members
- Helped shape the entity diagram with Chris, Jake, and Drew
- Put together the slides for our follow-up presentation on user stories and the entity diagram
- Drafted the mockup direction with the team, including the homepage layout and the "Possible Projects" table

**What I'm leaning on hard from my PM internship:**
The biggest carryover from my work at Acxiom is the user story format. When Mr. Turner described what he wanted, I translated it into "As a [user], I want [feature] so that [outcome]" right on the spot, which is the same structure I've been writing Jira tickets in all year. Estimating each story in hours (12 hours for admin CRUD, 6 for donor browsing, and so on) is also pulled directly from how my team works at Acxiom. Client communication is the other big one. Asking the right follow-up questions, like "What would make you confident that what we build is trustworthy and maintainable?" and "Is there anything you wish you were tracking but currently aren't?", is what surfaces the real requirements instead of the surface-level ones.

**Things I'm struggling with:**
- Pacing the team. Everybody works at different speeds and on different parts of the stack, so making sure nobody is waiting on me has been a constant adjustment.
- Translating between the database schema and the front-end mockup. The schema has clean entities like Donor, Opportunity, Proposal, Donation, and Review with clear relationships, but mapping those cleanly to a public-facing UI takes more thought than I expected.
- Resisting the urge to over-engineer. Mr. Turner wants something straightforward and trustworthy, not flashy.

**Things that still don't fully make sense yet:**
- How we're going to handle the "secure login (8-digit code)" piece on the admin side without falling into an auth rabbit hole
- The right balance between letting campus community members submit proposals freely and giving advancement staff enough control to filter out junk submissions

**Looking forward:**
- Wiring up the first working pages with the backend
- Bringing a clickable demo to the second client meeting
- Tightening the Hendrix orange styling so the mockup actually looks like it belongs to the school
- Getting Mr. Turner's reaction to seeing real data flow through the system

**Mockup screenshot:**

Here is where we landed on the homepage mockup, with the search bar, the "What is this? / How do I start? / Why care?" intro sections, and the "Possible Projects" table:

![Hendrix Advancement Homepage Mockup]({{ '/assets/images/mockup.png' | relative_url }})

Plenty still to build, but we have a clear shape now and a client who knows what he wants. That's a good place to be.