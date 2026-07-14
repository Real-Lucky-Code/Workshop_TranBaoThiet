---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

## Week 10 Goals

* Finalize the architecture design and initialize the development environment for the project.
* Build the Backend foundation following the Spring Boot model with a layered architecture.
* Design the data model, build the Entities, and establish the database access layer.
* Deploy the authentication (Authentication) and authorization (Authorization) mechanisms using Spring Security.
* Develop the initial business functions and integrate the user interface using Thymeleaf.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Review, edit, and finalize the deployment architecture diagram of the project on AWS Cloud.<br>- Initialize the project source code and configure the development environment with Java 21, Spring Boot 4, and Maven.<br>- Establish the MySQL database connection and configure the initial application parameters. | 22/06/2026 | 22/06/2026 | https://docs.spring.io/spring-boot/index.html |
| 3 | - Build the data layer (Data Layer) of the system.<br>- Design and build core Entities including User, Facility, Field, Booking, and ExtraService.<br>- Establish relationships between Entities according to the database model.<br>- Build the Repository layer using Spring Data JPA and the Service layer to handle business logic and interact with the database. | 23/06/2026 | 23/06/2026 | https://docs.spring.io/spring-data/jpa/reference/index.html |
| 4 | - Build the authentication and authorization mechanism using Spring Security.<br>- Configure Authentication and Authorization for the system.<br>- Develop registration, login, and authorization functions for User, Owner, and Admin roles.<br>- Test the operation of the security mechanism against basic functions. | 24/06/2026 | 24/06/2026 | https://docs.spring.io/spring-security/reference/index.html |
| 5 | - Develop the business layer (Business Layer) for the sports facility management function.<br>- Build APIs and Business Logic for facility creation, sports field management, and basic administrative functions.<br>- Integrate the user interface using Thymeleaf for login, registration, and facility management pages.<br>- Test the processing flow between the interface, business layer, and database. | 25/06/2026 | 25/06/2026 | No documentation |
| 6 | - Test, adjust, and finalize the functions deployed during the week.<br>- Test registration, login, authorization, and facility management functions.<br>- Summarize the project development progress.<br>- Update the Week 10 Worklog on the reporting.<br>- Plan the deployment of field booking and online payment functions for the following week. | 26/06/2026 | 26/06/2026 | No documentation |

## Week 10 Achievements

### Knowledge

* Understood the process of building a Spring Boot application according to the layered architecture model (Layered Architecture).
* Grasped how to organize Entity, Repository, Service, and Controller layers within an application.
* Understood the authentication (Authentication) and authorization (Authorization) mechanisms using Spring Security.
* Grasped the process of connecting to and manipulating the MySQL database via Spring Data JPA.

### System Design

* Finalized the deployment architecture diagram of the project on AWS Cloud.
* Built the data model and core Entities of the system.
* Established relationships between Entities as a foundation for developing business functions.

### Deployment

* Successfully initialized the Spring Boot project and configured the development environment.
* Completely built the Repository and Service layers to serve database access.
* Deployed registration, login, and authorization functions for User, Owner, and Admin roles.
* Developed sports facility management functions and integrated the user interface using Thymeleaf.
* Tested and finalized foundational functions before deploying more complex business logic.

### Skills

* Practiced Backend application development skills using Spring Boot.
* Improved the capability to design data models and build software architecture according to the layered model.
* Practiced integrating database, security, and interface within the same system.
* Formed a workflow of developing, testing, and finalizing functions according to each phase of the project.