---
title: "Week 1 - JPA Basics"
date: 2026-08-17
draft: false
weight: 1
---

# Week 1 - JPA Basics

In the first week I worked with JPA and learned how Java can work together with a database.

The main thing I learned was ORM. Instead of writing SQL all the time, I can create Java classes that represent tables in the database. JPA and Hibernate then handle a lot of the connection between the Java code and the database.

I also learned how to create entities using annotations like `@Entity`, `@Id` and `@GeneratedValue`.

Another important part was CRUD, where I worked with creating, reading, updating and deleting data. I used `EntityManager` for this and also learned about the DAO pattern, so the database code can be kept separate from the rest of the application.

We also worked a bit with JPQL and Lombok. JPQL is used to query entities instead of working directly with database tables, and Lombok helps remove some repeated code like getters, setters and constructors.

Overall, this week helped me understand JPA better and how it can make it easier to work with databases in Java.

## Exercises

During the week I worked on different exercises to practice JPA and database operations. One of the exercises was pushed on github as the "Codelab" exercise every wednesday.

[Week 1 exercises on GitHub](https://github.com/AmaanM3/CodelabWeek1)