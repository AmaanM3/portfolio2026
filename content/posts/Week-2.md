---
title: "Week 2 - JPA Relations"
date: 2026-08-24
draft: false
weight: 2
---

# Week 2 - JPA Relations

In week 2 I continued working with JPA, but this time the main focus was relationships between entities.

I learned about the different types of JPA relationships such as `@OneToOne`, `@OneToMany`, `@ManyToOne` and `@ManyToMany`. These relations are used when different entities in the database need to be connected to each other.

One example I worked with was a student and course system, where multiple students can belong to one course. For this I used a `@ManyToOne` relation from the Student entity to the Course entity.

I also learned more about unidirectional and bidirectional relationships. This helped me understand that a relationship does not always need to work both ways, and that it is often better to keep the relations as simple as possible.

Another topic was cascade types, which control what should happen to related entities when an entity is created, updated or deleted. I learned that cascade should be used carefully and only when it makes sense.

We also continued working with DAO classes and JPQL to save, update and retrieve related data from the database.

Overall, this week gave me a better understanding of how entities can be connected and how relationships between database tables can be represented in Java whereas before we have only worked on this in databases.

## Exercises

During the week I worked with JPA relations in a small student, course and teacher system.

[Week 2 exercises on GitHub](https://github.com/AmaanM3/CodelabWeek2.1)