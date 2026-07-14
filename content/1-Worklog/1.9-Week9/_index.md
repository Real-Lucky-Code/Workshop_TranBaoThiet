---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

## Week 9 Goals

* Determine the topic, scope, and deployment direction of the practical project in the internship program.
* Analyze business requirements and core functions of the system.
* Select the Technology Stack and AWS services suitable for the project's requirements.
* Design the High-Level Architecture as a foundation for the system deployment process.
* Prepare a plan for building AWS infrastructure and developing the application in the upcoming weeks.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Determine the project topic and scope: **Online sports field booking system**.<br>- Analyze the system's main functions, including field search, booking, sports facility management, and online payment.<br>- Select the Technology Stack for the project, including Java 21, Spring Boot 4 (Spring MVC, Spring Security), Thymeleaf, and MySQL. | 15/06/2026 | 15/06/2026 | No documentation |
| 3 | - Analyze the system's business requirements.<br>- Build main operational workflows, including:<br>&emsp;+ Booking workflow.<br>&emsp;+ Online payment workflow (VNPay/MoMo).<br>&emsp;+ Administration workflow for Admins and Field Owners.<br>- Identify requirements for Scalability, Security, and High Availability as a basis for AWS infrastructure design. | 16/06/2026 | 16/06/2026 | No documentation |
| 4 | - Design the AWS infrastructure architecture for the project.<br>- Select networking and compute services including Amazon VPC (Public/Private Subnets, Internet Gateway, NAT Gateway), Amazon EC2, Auto Scaling Group, and Application Load Balancer (ALB).<br>- Select Amazon RDS for MySQL (Primary/Standby) and Amazon S3 to store Static Assets via S3 Gateway Endpoint.<br>- Select AWS WAF, Amazon CloudWatch, and Amazon SNS to enhance system security, monitoring, and alerting. | 17/06/2026 | 17/06/2026 | https://aws.amazon.com/vi/what-is/architecture-diagramming/ |
| 5 | - Design the High-Level Architecture diagram of the system on the AWS Cloud platform.<br>- Identify user access workflows and communication workflows between system components.<br>- Evaluate the designed architecture's ability to meet performance, scalability, security, and availability requirements. | 18/06/2026 | 18/06/2026 | https://youtu.be/l8isyDe-GwY?si=FO9X7Zn1cscmuB1L |
| 6 | - Review, evaluate, and finalize the system's architecture diagram.<br>- Reach a consensus on the AWS infrastructure deployment plan for the project.<br>- Update the Week 9 Worklog on the reporting.<br>- Plan the initialization of AWS infrastructure and source code development for the following week. | 19/06/2026 | 19/06/2026 | No documentation |

## Week 9 Achievements

### Knowledge

* Understood the process of analyzing requirements and designing architecture for a project deployed on the AWS platform.
* Grasped the role of AWS services in building a web system that meets performance, scalability, security, and availability requirements.
* Understood the relationship between the network tier, application tier, database, and monitoring services in AWS architecture.

### System Design

* Completed defining the project's scope, functions, and technology stack.
* Analyzed the system's main business workflows as a basis for the deployment process.
* Completed designing the High-Level Architecture diagram of the system on AWS Cloud.
* Identified the AWS services to be used throughout the project development process.

### Deployment

* Selected an AWS infrastructure deployment plan suitable for the system's requirements.
* Finalized the architecture design and prepared an infrastructure deployment plan for the development phase.
* Built the initial foundation to serve the application development and deployment process in the upcoming weeks.

### Skills

* Practiced skills in analyzing business requirements and designing system architecture.
* Improved the ability to select technologies and AWS services suitable for real-world problems.
* Formed a system design mindset oriented toward meeting requirements for scalability, security, and high availability.
* Practiced planning and preparation skills prior to deploying a project on the AWS Cloud platform.