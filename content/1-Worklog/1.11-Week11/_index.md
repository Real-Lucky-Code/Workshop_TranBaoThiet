---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

## Week 11 Goals

* Finalize the core business operations of the online sports field booking system.
* Integrate the online payment gateway and build the user notification system.
* Fully develop the functionalities dedicated to Field Owners (Owners) and Administrators (Admins).
* Complete the user interface and test the entire system on the development environment.
* Prepare the application version ready for deployment onto the AWS infrastructure in the following week.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Develop and finalize the booking business workflow (Booking Workflow).<br>- Build a mechanism to check field availability by time slots, handle booking schedule conflicts, operating hours, and blocked time slots.<br>- Develop the functionality to select accompanying services and calculate the total value of booking orders on the localhost environment. | 29/06/2026 | 29/06/2026 | No documentation |
| 3 | - Integrate the online payment gateway (VNPay/MoMo) into the system.<br>- Build the workflow for creating payment links, handling Redirects and Callbacks to update transaction and booking order statuses.<br>- Finalize the notification system (Notification) to send booking order statuses to customers and field owners after transactions are completed. | 30/06/2026 | 30/06/2026 | https://miniai.vn/tich-hop-thanh-toan-vnpay/ |
| 4 | - Finalize the interface and business operations for Field Owners (Owner Dashboard).<br>&emsp;+ Manage sports facility and field information.<br>&emsp;+ Approve or reject booking cancellation requests.<br>- Finalize the interface and business operations for Administrators (Admin Dashboard).<br>&emsp;+ Approve newly registered sports facilities.<br>&emsp;+ Manage user account statuses (Ban/Unban). | 01/07/2026 | 01/07/2026 | No documentation |
| 5 | - Finalize the user interface using Thymeleaf.<br>&emsp;+ Sports facility details page.<br>&emsp;+ Booking history.<br>&emsp;+ Review/Rating functionality and wishlist.<br>- Perform comprehensive end-to-end testing (End-to-End Testing) of functional flows from Backend to Frontend on the localhost environment.<br>- Fix arising bugs and finalize data processing logic. | 02/07/2026 | 02/07/2026 | https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html |
| 6 | - Review and finalize the application version operating stably on the localhost environment.<br>- Re-check all main system functions before deploying to AWS.<br>- Summarize the project development progress during the week.<br>- Update the Week 11 Worklog on the report.<br>- Plan the system deployment onto the AWS infrastructure for the following week. | 03/07/2026 | 03/07/2026 | No documentation |

## Week 11 Achievements

### Knowledge

* Understood the process of building and finalizing core business operations in an online sports field booking system.
* Grasped the process of integrating an online payment gateway and handling transaction flows between the system and the payment service.
* Understood the mechanism for building a notification system and updating booking order statuses in real-time.
* Understood the comprehensive end-to-end testing process (End-to-End Testing) prior to system deployment.

### System Development

* Finalized the booking workflow with a schedule verification mechanism, conflict resolution, and cost calculation.
* Successfully integrated the online payment gateway and built the notification system for users.
* Finalized the functionalities dedicated to Field Owners (Owners) and Administrators (Admins).
* Completed the user interface and fully connected Frontend, Backend, and the database.

### Deployment

* Tested all functionalities on the localhost environment and corrected arising bugs.
* Finalized a stable application version, ready for the deployment process onto the AWS infrastructure.
* Prepared the deployment plan and AWS environment configuration for the next phase of the project.

### Skills

* Practiced skills in developing complex business logic in Spring Boot applications.
* Improved the capability to integrate third-party services such as online payment gateways.
* Practiced integration testing (Integration Testing) and comprehensive end-to-end testing (End-to-End Testing) for the system.
* Formed a workflow of finalizing, testing, and preparing for the deployment of a web application on the AWS Cloud platform.