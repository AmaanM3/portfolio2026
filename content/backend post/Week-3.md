---
title: "Week 3 - Data Integration"
date: 2026-08-31
draft: false
weight: 3
---

# Week 3 - Data Integration

In week 3 I worked with data integration and learned how to get data from an external API and use it in a Java application.

I worked with the TMDB API, where I used `HttpClient` to send requests and get movie data back as JSON.

I also learned how DTOs can be used to only keep the data I actually need from the API. In my exercise I used classes like `MovieDTO` and `MovieResponseDTO` for this.

Another thing I worked with was Jackson and `ObjectMapper`, which makes it possible to convert JSON into Java objects. This made the API data much easier to work with in the code.

I also learned that API keys should not be written directly in the code or pushed to GitHub, so they can instead be stored as environment variables.

In my exercise I created a `MovieService` that was responsible for fetching and working with movie data from the API.

Overall, this week helped me understand better how a Java application can communicate with an external API and use the data it gets back.

## Exercises

For this week I made a small project using the TMDB API as my wednesday assignment.

[Week 3 exercise on GitHub](https://github.com/AmaanM3/CodelabWeek3)