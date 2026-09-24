---
title: "Week 4 - Concurrency"
date: 2026-09-07
draft: false
weight: 4
---------

# Week 4 - Concurrency

In week 4 I worked with concurrency and learned how threads work in Java.

I learned that threads can be used to run multiple tasks at the same time insteead of doing everything one by one.

We also worked with `ExecutorService`, which can be used to manage multiple threads.

Another thing I learned about was race conditions. This can happen when two threads try to use or change the same data at the same time, which can cause problems.

In our backend project "DriveApp", I added threads to the booking system. We made a test where two students tried to book the same driving lesson at the same time.

I used `ExecutorService` with two threads and made the `bookLesson` method `synchronized`, so only one student could book the lesson.

Overall, this week helped me understand concurrency better and how threads can be useful in a real backend project.

## Exercises

During the week I worked with concurrency in our DriveApp backend project.

I added threads to the booking system so two students could not book the same driving lesson at the same time.

[DriveApp backend project on GitHub](https://github.com/Musa-909/DriveApp)
