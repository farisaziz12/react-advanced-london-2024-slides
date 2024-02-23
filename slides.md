---
theme: seriph
background: https://www.queensu.ca/gazette/sites/gazettewww/files/assets/WEB%20Coding%20arnold-francisca-nPhl2x4fk2s-unsplash.jpg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## React Advanced London 2024

drawings:
  persist: false
defaults:
  foo: true
transition: slide-left
title: React Advanced London 2024
mdc: true
---

# Data Fetching Unleashed

Next.js, React Query and their BFF

---
transition: fade-out
---

# Who Am I?

- **Faris Aziz**
- 👨‍💻 **Engineering Manager @ Navro** - Fintech building an API & Portal to smoothly navigate your growth into foreign
  markets with maximum coverage and minimal hassle. Enabling global payouts in 170+ countries with 130+ currencies and collections in 35+ currencies.

- 🇨🇭🇵🇰 **From** - Switzerland & Pakistan
- 🕸️ **Previous Experience** - Connected TV, Digital Asset Management, FinTech & Fitness Tech
- 📚 **Interests** - Web Performance & Developer Experience
- 📩 **Open Source** - Raycast

---
layout: default
---

# Setting the Stage

- **There is no one size fits all** - Every project has its own unique requirements and this talk is not about finding the one true way.
- **This is not a tutorial** - We will not be building a full-fledged application, but rather focusing on the concepts and patterns.
- **We will not cover everything** - There are many other libraries and patterns that are not covered in this talk. This is just a starting point.
- **There is such a thing as Premature Optimization** - These patterns and libraries are powerful, but it's important to understand if they're even needed in the first place.

---
transition: slide-up
---
# Problem Statement

### What challenges do developers face in creating a seamless user experience due to complex data fetching and management?

---
transition: slide-up
---

# Why Bother?

- Milliseconds are crucial for user satisfaction in the digital space.
- Quick page load times are directly related to user happiness.
- A 2022 study found pages that load in 0-2 seconds (golden window) have the highest conversion rates.
- Google research shows a 32% increase in the likelihood of a bounce rate when page load time increases from 1 to 3 seconds.

---
transition: slide-up
---

# Technologies

-  **NextJS** - The React Framework
    - **Server Side Rendering** - Pre-rendering pages on the server
    - **Static Site Generation** - Pre-rendering pages at build time
    - **File-based Routing** - Routing based on the directory structure
    - **API Routes** - Quickly create API endpoints

-  **React Query** - Powerful asynchronous state management
    - **Automatic Caching and Background Updates** - Fetch, cache and update data in your React components
    - **Optimistic Updates** - Update the UI before the server responds
    - **Pagination and Infinite Loading** - Load more data as the user scrolls
    - **Prefetching** - Prefetch data before it's needed
    - **Built-in Query Invalidations** - Automatically refetch data when it's stale


---
transition: slide-up
---


# Bare Bones Data Fetching

- **Scenario:** Our frontend team needs to design a dashboard chart that displays the distribution of birthdays for the top 5000 users in the system.
- **Data Source:** The data is available via an API which returns a list of users with all their data.
- **Limitation:** The backend team is unable to provide a new endpoint or data warehouse that returns the required data format and there is a limit of 1000 users returned for each request.

---
transition: slide-up
---

# Demo 1

- **Model 1:** https://app.eraser.io/workspace/x9l3uRQvK7iwu2ET8eVK?origin=share&elements=qA4b68WYgk7xd0RUs0IbuA
- **View:** http://localhost:3000/example-2

---
transition: slide-up
---

# Backend For Frontend (BFF) - Transformation Bridge / Aggregation Proxy

- **Adaptability to Platform Requirements:** The BFF pattern allows developers to create backend services that cater to each platform's unique requirements, data formats, and interaction patterns, leading to better UX and more efficient resource usage.
- **Decoupling of Concerns:** By delegating data aggregation and transformation tasks to the backend, the BFF pattern promotes a clear separation of concerns between frontend and backend development.
- **Optimized Performance**: By providing a dedicated backend for each frontend, the BFF pattern can optimize data aggregation, transformation, and caching, resulting in reduced latency, smaller payload sizes, and better overall performance.
- **Streamlined API Evolution:** The BFF pattern simplifies API evolution management, as developers can introduce new features, make changes, or deprecate outdated functionality without impacting other platforms.

---
transition: slide-up
---

# Payload Optimization

```json
{
  "id": "97ea75b2-f94c-381b-ad21-a6901c26093a",
  "firstName": "Rosina",
  "lastName": "Muller",
  "dateOfBirth": "1998-01-05",
  "profilePicture": "http://placeimg.com/640/480/any",
  "phone": "+5372196581565",
  "email": "upton.salvador@yahoo.com",
  "address": "575 Nelson Underpass Suite 096",
  "city": "Lake Kailee",
  "country": "Portugal",
  "latitude": -31.179547,
  "longitude": -106.76482,
  "company": "Navro",
  "jobTitle": "Senior Developer",
  "bio": "Lorem ipsum dolor..."
}
```

---
transition: slide-up
---


# Payload Optimization

```json
{
  "id": "97ea75b2-f94c-381b-ad21-a6901c26093a",
  "firstName": "Rosina",
  "lastName": "Muller",
  "dateOfBirth": "1998-01-05",
}
```
---
transition: slide-up
---

# Demo 2

- **Model 2:** https://app.eraser.io/workspace/x9l3uRQvK7iwu2ET8eVK?origin=share&elements=Ggh2Uu7Ml-iupuV0AbvMtQ
- **View:** http://localhost:3000/example-1

---
transition: slide-up
---

# Demo 3

- **Model 3:** https://app.eraser.io/workspace/x9l3uRQvK7iwu2ET8eVK?origin=share&elements=wHKWjQC_u2F1QU9bHAseyQ
- **View:** http://localhost:3000/


---
transition: slide-up
---

# That's it

- Website: https://faziz-dev.com/

---
transition: slide-up
---
