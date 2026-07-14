---
title: "Blog 1: Offline-First Application"
date: 2024-07-04
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# BUILDING AN OFFLINE-FIRST APPLICATION WITH AWS AMPLIFY, TANSTACK, APPSYNC, AND MONGODB ATLAS

**INTRODUCTION:**
In the modern application world, users expect a seamless experience even without a network connection. This is why Offline-First and Optimistic UI have become two crucial design philosophies: the application does not wait for a server response to update the interface, but updates immediately based on predicted results, while automatically synchronizing when the connection is restored.

This article presents how to build an offline-first application with Optimistic UI by combining AWS Amplify, AWS AppSync, and MongoDB Atlas — a powerful toolset that allows for rapidly building full-stack serverless applications.

**KEY TAKEAWAYS:**

- **4 core architectural components of the application:** 
    - MongoDB Atlas serves as the database.
    - AWS Amplify is the full-stack framework.
    - AWS AppSync manages the GraphQL API layer.
    - AWS Lambda Resolver handles serverless logic.
    - Amazon Cognito handles user authentication.
- **The role of TanStack Query — the heart of Offline Caching:** TanStack Query is an asynchronous state management library for TypeScript/JavaScript, supporting React, Vue, Svelte, Angular, and many other frameworks. It simplifies fetching, caching, synchronizing, and updating server state in web applications. When offline, mutations are queued and automatically retried when the network recovers — while the UI still displays results immediately thanks to the local cache.
- **How the Optimistic UI mechanism works:** The sample application renders the results of CRUD operations on MongoDB Atlas immediately on the UI before the request completes, improving the user experience. When an error occurs, TanStack Query automatically rolls back the UI to its previous state based on a saved snapshot.
- **Practical benefits:** This approach reduces the need to display loading screens, improves performance through faster data access, ensures reliability when the app is offline, and optimizes operational costs.
- **Conflict Resolution:** The application implements a simple conflict resolution mechanism based on the "first-come, first-served" principle — MongoDB Atlas saves updates in the order they are received, and later updates will overwrite earlier ones. This is a crucial point to consider if your application has a high conflict frequency, which would require more complex strategies.

![Article Illustration](/images/3-Blogs/anh_blogs_1.png)

**CONCLUSION**
Combining AWS Amplify, TanStack Query, AppSync, and MongoDB Atlas opens up a practical approach to building offline-first applications without having to build the entire caching infrastructure from scratch. Amplify Hosting provides a git-based workflow that allows for atomic deployment, ensuring that updates are only applied after the entire deployment process is complete.

This is an architecture worth referencing for any team looking to enhance user experience under unstable network conditions — especially suitable for mobile apps, field services, or any context where a continuous internet connection cannot be guaranteed.

Have you ever implemented Offline-First or Optimistic UI in your project? Share your experiences and the challenges you faced in the comments section!

---
**Original article link:** [Offline Caching with AWS Amplify, TanStack, AppSync, and MongoDB Atlas](https://aws.amazon.com/blogs/mobile/offline-caching-with-aws-amplify-tanstack-appsync-and-mongodb-atlas/)