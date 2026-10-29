
---
title: "Exam Portfolio"
date: 2026-10-27
draft: false
weight: 1
description: "My third semester backend exam portfolio"
showDate: true
showReadingTime: true
showWordCount: true
showAuthor: false
---


# DriveApp – Driving School Management System

DriveApp is our third semester backend project, which I developed together with Musa.

The idea behind DriveApp was to create a system for a driving school where students, instructors, driving lessons and bookings could be managed in one place.

We built the application using Java, Javalin, Hibernate/JPA and PostgreSQL.

During the semester, we worked on the project step by step and added new features as we learned about different backend topics.

We started by setting up our database and working with JPA. Later, we added REST API endpoints, integrated Google Gemini as an AI driving assistant, worked with security using JWT and BCrypt, and created automated tests.

In the end, we also worked with Docker, GitHub Actions and deployed our backend to DigitalOcean.

On this page, I will go through how we developed DriveApp throughout the semester, what I learned and how we used the different technologies in our project.

---

## Project Links

**GitHub Repository**

[DriveApp Github Source Code](https://github.com/Musa-909/DriveApp)

**Deployed Application**

[DriveApp API](https://driveapp.website)


**API Health Check**

[To check if DriveApp is running](https://driveapp.website/api/health)

---

## Project Development

During the semester, we worked on DriveApp step by step and used what we learned from the different backend topics in class.

Each week, we learned something new that we could use to improve our application. We started with databases and JPA, and later worked with REST APIs, testing, security and deployment.

The table below shows the topics we worked with each week and how we used them in DriveApp.

| Week | Topic | How we used it in DriveApp |
|---|---|---|
| Week 1 | JPA Basics | We used Hibernate, JPA and PostgreSQL to set up our database and create our first entities and DAO classes. |
| Week 2 | JPA Relations | We created relationships between Student, Instructor, Lesson and Booking, and worked with JPQL queries. |
| Week 3 | Data Integration | We integrated Google Gemini using Java HttpClient, JSON and DTOs to create our AI driving assistant. |
| Week 4 | Concurrency | We learned about threads, race conditions and synchronized, and used CompletableFuture to handle asynchronous requests to Google Gemini. |
| Week 5 | REST API | We used Javalin to create routes, controllers and endpoints for students, instructors, lessons and bookings. |
| Week 6 | REST Testing | We used JUnit, REST Assured and Testcontainers to test our API endpoints and database operations. |
| Week 7 | Security | We implemented BCrypt, JWT authentication and role based access control to protect our API. |
| Week 8 | Deployment & DevOps | We used Docker, GitHub Actions and DigitalOcean, and followed the deployment guide to connect our domain through DanDomain. |

Below, I will go through each week in more detail and explain what we worked on, what I learned and how DriveApp developed throughout the semester.

---



## Selected Blog Posts

Below are my blog posts from the third semester, where I have documented what we worked on in class and what I learned each week.

These posts show my learning throughout the semester, while the sections below explain how we used these topics in DriveApp.

### Weekly Blog Posts

* [Week 1 - JPA Basics]({{< relref "posts/Week-1.md" >}})
* [Week 2 - JPA Relations]({{< relref "posts/Week-2.md" >}})
* [Week 3 - Data Integration]({{< relref "posts/Week-3.md" >}})
* [Week 4 - Concurrency]({{< relref "posts/Week-4.md" >}})
* [Week 5 - REST API]({{< relref "posts/Week-5.md" >}})
* [Week 6 - REST Testing]({{< relref "posts/Week-6.md" >}})
* [Week 7 - Security]({{< relref "posts/Week-7.md" >}})
* [Week 8 - Deployment]({{< relref "posts/Week-8.md" >}})

---

## Week 1 – JPA Basics

In week 1, we started working on DriveApp and focused on setting up the backend and database.

We used Java, Maven, Hibernate/JPA and PostgreSQL. We also started creating our first entities and DAO classes to manage data in the database.

### What we worked on

* Set up our Java project with Maven
* Connected our application to PostgreSQL
* Configured Hibernate and JPA
* Created Student and Instructor entities
* Worked with DAO classes and CRUD operations
* Used EntityManager to communicate with the database

### What I learned

This week I learned how JPA and Hibernate work together with PostgreSQL and how we can use entities to represent database tables.

I also got a better understanding of DAO classes and why it is useful to separate database operations from the rest of the application.

### Result

By the end of the week, we had the basic database setup ready and could start managing data through our DAO classes.

This gave us a good starting point for developing the rest of DriveApp.



---

## Week 2 – JPA Relations

In week 2, we continued working on DriveApp and focused on creating relationships between our entities.

We worked with Student, Instructor, Lesson and Booking, and connected them using JPA relationships.

This was important for our project because students need to be connected to their bookings, and driving lessons need to be connected to instructors.

### What we worked on

* Created relationships between our entities
* Worked with @OneToMany and @ManyToOne
* Connected students, instructors, lessons and bookings
* Used foreign keys to connect database tables
* Worked with JPQL queries
* Updated our DAO classses
* Created JUnit tests for CRUD operations and relationships

### What I learned

This week I learned how relationships work in JPA and how we can connect different entities in our database.

I also learned how to use JPQL to retrieve data and how important it is to structure database relationships correctly.

Working with JUnit tests also helped me understand how to check that our database operations work as expected.

### Result

By the end of the week, we had created relationships between the different entities in DriveApp.

We could now connect students to bookings and instructors to driving lessons.

This made our database more useful and gave us a better foundation for building the booking system later in the project.



---

## Week 3 – Data Integration & Gemini AI

In week 3, we worked with data integration and started adding Google Gemini to DriveApp.

We wanted to create an AI driving assistant where students could ask questions about driving theory, traffic rules and road safety.

To make this work, we used Java HttpClient to communicate with the Gemini API and JSON to send and receive data.

### What we worked on

* Integrated Google Gemini into DriveApp
* Created the DrivingAiService class
* Used Java HttpClient to send HTTP requests
* Worked with JSON and Jackson ObjectMapper
* Created DTO classes to handle the Gemini response
* Worked with serialization and deserialization
* Created tests for our AI service

### What I learned

This week I learned how to connect our Java application to an external API.

I also got a better understanding of how JSON works and how we can use Jackson to convert JSON into Java objects.

Working with DTOs helped me understand how to structure data when communicating with external services.

### Result

By the end of the week, we had implemented our AI driving assistant using Google Gemini.

Our application could now send questions to Gemini and receive answers that could be used in DriveApp.

This was an important feature because it added something extra to our driving school system.



---

## Week 4 – Concurrency & Booking System

In week 4, we worked with concurrency and multithreading in Java.

We learned how multiple threads can run at the same time and what problems can happen when different users try to access or change the same data.

This was relevant for DriveApp because we have a booking system where multiple students might try to book the same driving lesson.

We also worked with CompletableFuture in our Gemini AI integration to handle asynchronous HTTP requests.

### What we worked on

* Learned about threads and multithreading in Java
* Worked with Runnable and ExecutorService
* Learned about race conditions
* Worked with synchronized
* Implemented booking logic in BookingController and BookingDAOImpl
* Added checks to prevent students from booking an already booked lesson
* Worked with CompletableFuture in our DrivingAiService
* Tested different booking scenarios

### What I learned

This week I learned how concurrency works and why it is important when multiple users are using the same application.

I also learned about race conditions and how synchronized can help prevent multiple threads from accessing the same critical section at the same time.

Working with CompletableFuture helped me understand how asynchronous operations can be used when communicating with external APIs like Google Gemini.

### Result

By the end of the week, we had improved our booking system by checking if a driving lesson was already booked before creating a new booking.

We also worked with concurrency to better understand how to handle multiple requests.

This helped us make DriveApp more reliable and gave us a better understanding of concurrency in backend applications.



---

## Week 5 – REST API & Javalin

In week 5, we worked with REST APIs and started making our DriveApp backend accessible through HTTP requests.

Until now, we had mainly worked with our database, entities and DAO classes. We now wanted to make it possible to interact with our application through API endpoints.

We used Javalin to create our REST API and connected our controllers to the DAO classes.

### What we worked on

* Added Javalin to our project
* Created routes and controllers
* Worked with GET, POST, PUT and DELETE requests
* Created endpoints for students, instructors, lessons and bookings
* Connected our controllers to the DAO layer
* Used DTOs to handle request and response data
* Added validation for incoming requests
* Worked with HTTP status codes
* Added error handling and logging
* Documented our API endpoints in the README

### What I learned

This week I learned how REST APIs work and how we can use HTTP methods to communicate with our backend.

I also learned why it is important to separate our application into different layers.

Routes define the endpoints, controllers handle the requests, and DAO classes communicate with the database.

Working with DTOs also helped me understand how we can control what data is sent and received through our API.

### Result

By the end of the week, we had created a REST API for DriveApp using Javalin.

We could now manage students, instructors, driving lessons and bookings through HTTP requests.

This was an important step because our application was no longer only connected to the database but could also be accessed through API endpoints.




---

## Week 6 – REST Testing & Integration Tests

In week 6, we focused on testing our DriveApp backend to make sure everything worked as expected.

We had already worked with tests for our DAO classes, but now we also wanted to test our REST API endpoints.

We used JUnit and REST Assured to send HTTP requests and check if our API returned the correct responses.

We also worked with two separate databases, one for production and one for testing. This was important because we did not want our tests to affect the real data in our production database.

### What we worked on

* Used JUnit to create automated tests
* Used REST Assured to test our API endpoints
* Tested GET, POST, PUT and DELETE requests
* Checked HTTP status codes and JSON responses
* Tested both valid and invalid requests
* Created tests for students, instructors, lessons and bookings
* Worked with Testcontainers and PostgreSQL for database testing
* Used Testcontainers to automatically create temporary PostgreSQL 16 databases for testing
* Created shared DatabaseTest and ApiTest classes to automatically start the database and Javalin server
* Made sure our tests did not affect the production database
* Used test data without adding test users or bookings to production
* Tested our DAO classes and database operations
* Created tests for our Gemini AI integration
* Worked with error handling and different test scenarios

### What I learned

This week I learned how important automated testing is when developing a backend application.

I learned how to use REST Assured to test API endpoints without having to send requests manually.

I also got a better understanding of how Testcontainers can be used to test our application with PostgreSQL.

One important thing we worked on was separating our production database from our test environment.

At first, we used a separate local PostgreSQL test database, but later we improved our testing setup by using Testcontainers.

Testcontainers automatically creates temporary PostgreSQL databases when we run our tests. We also made our API tests start Javalin automatically and create their own test users.

This helped me understand why it is important to keep testing separate from production and how automated test environments can make testing easier and more reliable.

### Result

By the end of the week, we had added more automated tests to DriveApp.

We improved our testing setup by using Testcontainers to automatically create temporary PostgreSQL databases for our tests.

Our API tests can now start Javalin automatically on an available port and create their own test users without needing a manually configured test database.

This made our tests more independent and easier to run locally and through GitHub Actions. It also helped us keep test data separate from our production database and made DriveApp more reliable.


---

## Week 7 – Security, BCrypt & JWT

In week 7, we worked with security in DriveApp and focused on making our REST API more secure.

We wanted to make sure that students and instructors could log in safely and only access the features they were allowed to use.

To do this, we worked with BCrypt for password hashing and JWT for authentication.

### What we worked on

* Implemented BCrypt to hash passwords
* Created login functionality for students and instructors
* Worked with authentication and authorization
* Implemented JWT tokens for logged in users
* Created the JWTToken class
* Added security filters to protect our API endpoints
* Worked with different user roles such as STUDENT and INSTRUCTOR
* Added role based access control
* Added checks so students can only access their own information
* Created tests for BCrypt and JWT

### What I learned

This week I learned the difference between authentication and authorization.

Authentication is about checking who the user is, while authorization is about checking what the user is allowed to do.

I also learned why we should never store passwords as plain text and how BCrypt can be used to hash passwords before saving them in the database.

Working with JWT helped me understand how a user can log in and use a token to access protected API endpoints.

### Result

By the end of the week, we had added security to DriveApp using BCrypt, JWT and different user roles.

Students and instructors could now log in, and our backend could check their permissions before allowing access to protected endpoints.

This was an important part of the project because we needed to protect user information and make sure that users could only access the features they were allowed to use.




---

## Week 8 – Deployment & DevOps

In week 8, we worked with deployment and DevOps to make DriveApp available online.

Until now, we had mainly been running our application locally. We wanted to make our backend accessible through the internet so other people could use our API.

To do this, we followed the deployment guide from our course material and used Docker, GitHub Actions, DigitalOcean and DanDomain.

### What we worked on

* Created a Dockerfile for our Java application
* Worked with Docker images and containers
* Used Docker Compose to manage our application and database
* Created a GitHub Actions workflow
* Worked with CI/CD to automate building and testing
* Used Docker Hub to store our Docker images
* Followed the deployment guide from our course material
* Deployed DriveApp to a DigitalOcean server
* Configured PostgreSQL for our deployed application
* Worked with environment variables
* Used DanDomain to configure our domain and DNS settings
* Connected our domain to the DigitalOcean server
* Set up HTTPS for our API
* Tested our deployed REST API

### What I learned

This week I learned how to deploy a backend application and make it available online.

I learned how Docker can be used to package our application into a container so it can run in different environments.

Working with GitHub Actions also helped me understand how CI/CD works and how we can automate building and testing our application when we push changes to GitHub.

We also followed the deployment guide from our course material to get DriveApp up and running using DigitalOcean and DanDomain.

This helped me understand how to connect a domain to our server and how DNS settings work. It was also nice to see our application running online instead of only on localhost.

### Result

By the end of the week, we had deployed DriveApp to DigitalOcean and made our REST API available online.

Our backend can now be accessed through our domain:

[DriveApp API](https://driveapp.website)

We also had a GitHub Actions workflow that helped automate our build and testing process.

This was an important step because we went from running DriveApp locally to having a backend that could be accessed through the internet.


---

## Project Architecture & Technical Decisions

In DriveApp, we used a layered architecture to keep our backend organized and easier to maintain.

We separated our application into routes, controllers, DAO classes and services, so each part of the code has its own responsibility.

### REST API and Database

We used Javalin to create our REST API and handle HTTP requests for students, instructors, lessons and bookings.

We also used Hibernate/JPA and PostgreSQL to store our data. DAO classes handle the database operations, while DTOs control what data is sent and received through our API.

This made our code easier to understand and helped us avoid exposing sensitive information like passwords.

### Services and Booking Logic

We implemented our booking logic in BookingController and BookingDAOImpl. Before creating a booking, we check that the student and lesson exist and that the lesson has not already been booked.

We also created DrivingAiService to communicate with Google Gemini using Java HttpClient and CompletableFuture.

This separation helped us organize our code and keep the database operations separate from the API controllers.

### Separate Test and Production Databases

We decided to separate our production database from our automated testing environment.

Our deployed application uses a PostgreSQL database, while our automated tests use temporary PostgreSQL 16 databases created through Testcontainers.

We also created shared DatabaseTest and ApiTest classes to automatically start and stop the test database and Javalin server.

This means we can run our tests without manually creating a test database or starting the application ourselves.

This was important because we wanted to make sure our tests did not create test users or bookings in our production database.

### Security

We used BCrypt to hash passwords and JWT to authenticate users.

We also implemented roles for students and instructors to control which endpoints they could access.

We chose these solutions to protect user information and make our API more secure.

### Deployment

We used Docker to run our application in containers and GitHub Actions to automate building and testing.

We also followed the deployment guide from our course material and used DigitalOcean and DanDomain to get DriveApp online.

### What I learned

Working with DriveApp helped me understand why it is important to think about the structure of an application and not just make the code work.

I also learned how decisions about security, testing and deployment can make a backend more reliable and easier to maintain.


---

## Final Reflection

Throughout the semester, I have learned a lot about backend development by working on DriveApp together with Musa.

We started with JPA, Hibernate and PostgreSQL, and slowly built our application by adding REST APIs, testing, security and deployment.

One of the biggest things I learned was how the different parts of a backend application work together, from the database and DAO classes to controllers and API endpoints.

We also faced some challenges during the project, especially with testing and getting our application to work correctly with different database configurations.

For example, we initially used a separate local PostgreSQL ttest database, but later improved our testing setup by using Testcontainers. Our tests now automatically create temporary PostgreSQL databases and start Javalin on an available port.

We also worked on fixing issues with our tests and GitHub Actions. This helped me understand why automated testing and keeping the test environment separate from production are important.

Another challenge we had was with our domain from DanDomain. We had problems getting the DNS settings to work correctly, especially with the nameservers (NS1, NS2 and NS3).

We had to contact DanDomain several times and call back and forth to figure out what was wrong and get the domain connected correctly to our server.

This was a bit frustrating, but it helped me understand more about how domains, nameservers and DNS work when deploying an application.

Working on these problems helped me understand how important testing, debugging and having a good project structure are.

I also learned how to work with GitHub in a group and how to deploy a backend application using Docker and DigitalOcean.

Overall, DriveApp has helped me get a better understanding of backend development and how to build an application from the beginning to a working deployed system.

