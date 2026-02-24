---
layout: post
title: "Lab 6 - Data Modeling: Online Grocery Store Application"
date: 2026-02-24 10:00:00 -0600
---

In Lab 6, we planned the data model for an online grocery shopping app using user stories, an ER diagram, and a SQL schema.

### Assumptions I made
I assumed:
- Customers can have multiple orders over time (hence 1-to-many).
- Orders can be pickup or delivery (added IsPickup boolean).
- Items have fixed stock (QuantityAvailable), but no automatic decrement yet (future feature).
- No payment, login credentials, or user roles beyond basic info (kept it simple per lab description).
- One active/in-progress order per customer at a time (simplifies model).