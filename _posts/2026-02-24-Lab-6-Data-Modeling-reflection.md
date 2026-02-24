---
layout: post
title: "Lab 6 - Data Modeling: Online Grocery Store Application"
date: 2026-02-24 10:00:00 -0600
author: James Randle Jr
---

In Lab 6, we planned the data model for an online grocery shopping app using user stories, an ER diagram, and a SQL schema.

### Assumptions I made
I assumed:
- Customers can have multiple orders over time (hence 1-to-many).
- Orders can be pickup or delivery (added IsPickup boolean).
- Items have fixed stock (QuantityAvailable), but no automatic decrement yet (future feature).
- No payment, login credentials, or user roles beyond basic info (kept it simple per lab description).
- One active/in-progress order per customer at a time (simplifies model).

### User Stories (5)
1. As a new customer, I want to register an account with my name, address, and phone number so that I can save my details and place orders without re-entering info every time. (Size: 3 points, blocks order placement)
2. As a store owner, I want to add food items for sale with name, price, description, quantity available, and manufacturer so that customers can browse and buy what's in stock. (Size: 5 points, required before shopping)
3. As a registered customer, I want to start an order by selecting items, specifying quantity, special instructions, and substitution permission so that I can build my shopping list. (Size: 5 points, depends on registration and items)
4. As a registered customer, I want to choose a pickup or delivery time/date when finalizing my order so that the store knows when to prepare it. (Size: 3 points, depends on order started)
5. As a customer, I want to view my finalized order details (items, total, time, status) so that I can confirm what I ordered and when it's ready. (Size: 2 points, depends on finalizing order)


### Entity-Relationship Diagram (LucidChart)
Logical/conceptual model showing entities and crows-foot relationships:

![My Alt Text]({{ '/assets/images/Grocery Store ERD Chart - James Randle Jr.png' | relative_url }})

I used 4 entities (Customer, Item, Order, OrderItem) with 1-to-many relationships, matching the Boats example style from Dr. Goadrich.

### SQL Schema (Redgate Data Modeler)
Physical model with tables, data types, PKs, and FKs:

![My Alt Text]({{ '/assets/images/Online_Grocery_Shop_Application-2026-02-24_09-33.png' | relative_url }})

The schema has clear primary and foreign key relations (Order references Customer, OrderItem references Order and Item).


### Reflection
This lab was more about learning how to create tables and define relationships than actually implementing a full online grocery store application. The hardest part for me was forming the tables themselves in Redgate Data Modeler and figuring out how to get certain columns to become foreign keys and connect properly. The web interface was confusing at first (missing dropdowns, self-referencing loops, no obvious way to choose the parent table), and I spent a lot of time stuck until Dr. Goadrich helped in class. Once I got the drag-to-connect and References section working correctly, the lines appeared and the relationships linked up as intended.

I'm satisfied with the final SQL schema. It captures the one-to-many relationships cleanly, and the OrderItem junction table handles the many-to-many between orders and items without issues. This lab showed me how important it is to get the structure right before coding, and how much the tool can slow you down when you're still learning.

