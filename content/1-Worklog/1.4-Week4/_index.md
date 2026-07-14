---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

## Week 4 Goals

* Understand the web application deployment process using Amazon EC2 combined with Amazon RDS.
* Grasp how to configure the connection between the application and the database in the AWS environment.
* Learn the data backup and recovery process using Amazon RDS Snapshots.
* Understand the load balancing architecture with Elastic Load Balancing (ELB) and the resource scaling mechanism using Amazon EC2 Auto Scaling.
* Practice deployment, monitoring, and resource cleanup skills to optimize costs during practice.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| Monday | - Explore an overview of Amazon RDS and the lab content.<br>- Prepare the infrastructure for application deployment:<br>&emsp;+ Create an Amazon VPC.<br>&emsp;+ Create a Security Group for Amazon EC2.<br>&emsp;+ Create a Security Group for Amazon RDS.<br>&emsp;+ Create a DB Subnet Group to serve database deployment. | 11/05/2026 | 11/05/2026 | https://000005.awsstudygroup.com/ |
| Tuesday | - Deploy an Amazon EC2 Instance.<br>&emsp;+ Choose an Amazon Machine Image (AMI).<br>&emsp;+ Choose an Instance Type.<br>&emsp;+ Configure the VPC, Subnet, and Security Group.<br>&emsp;+ Launch and test connectivity to the EC2 Instance.<br>- Deploy an Amazon RDS Database Instance.<br>&emsp;+ Select the Database Engine.<br>&emsp;+ Set up credentials.<br>&emsp;+ Configure the DB Subnet Group and network connection.<br>&emsp;+ Check the operating status of the RDS Instance. | 12/05/2026 | 12/05/2026 | https://000005.awsstudygroup.com/ |
| Wednesday | - Deploy a web application using Amazon EC2 and Amazon RDS.<br>&emsp;+ Install the environment and required software packages on EC2.<br>&emsp;+ Establish a connection between the application and Amazon RDS.<br>&emsp;+ Test the application running on a browser.<br>- Perform database backup and recovery.<br>&emsp;+ Create an Amazon RDS Snapshot.<br>&emsp;+ Restore Amazon RDS from a Snapshot.<br>- Clean up resources.<br>&emsp;+ Delete the Amazon RDS Database.<br>&emsp;+ Delete the Amazon EC2 Instance.<br>&emsp;+ Delete the DB Subnet Group, Security Groups, and Amazon VPC. | 13/05/2026 | 13/05/2026 | https://000005.awsstudygroup.com/ |
| Thursday | - Learn about Elastic Load Balancing and Amazon EC2 Auto Scaling architecture.<br>- Prepare the infrastructure for Auto Scaling deployment.<br>&emsp;+ Set up the network infrastructure.<br>&emsp;+ Launch an Amazon EC2 Instance.<br>&emsp;+ Provision an Amazon RDS Database Instance.<br>&emsp;+ Set up data for the database.<br>&emsp;+ Deploy the Web Server.<br>&emsp;+ Prepare CloudWatch Metrics for Predictive Scaling.<br>&emsp;+ Create a Launch Template. | 14/05/2026 | 14/05/2026 | https://000006.awsstudygroup.com/ |
| Friday | - Set up an Elastic Load Balancer.<br>&emsp;+ Create a Target Group.<br>&emsp;+ Create an Application Load Balancer.<br>&emsp;+ Test the traffic distribution capability.<br>- Create an Amazon EC2 Auto Scaling Group.<br>- Test Auto Scaling policies.<br>&emsp;+ Manual Scaling.<br>&emsp;+ Scheduled Scaling.<br>&emsp;+ Dynamic Scaling.<br>&emsp;+ Monitor Predictive Scaling via CloudWatch Metrics.<br>- Clean up all resources after completing the lab.<br>- Summarize the knowledge learned during the week.<br>- Update the Week 4 Worklog on the reporting.<br>- Plan learning and practice activities for the following week. | 15/05/2026 | 15/05/2026 | https://000006.awsstudygroup.com/ |

## Week 4 Achievements

### Knowledge

* Understood the web application deployment process on Amazon EC2 combined with Amazon RDS.
* Grasped how to configure the connection between the application and the database in the AWS environment.
* Understood the operating principles of Elastic Load Balancing (ELB) and Amazon EC2 Auto Scaling.
* Understood the database backup and recovery process using Amazon RDS Snapshots.

### Practice Environment

* Successfully deployed an Amazon EC2 Instance and an Amazon RDS Database Instance.
* Established a connection between the web application on EC2 and the Amazon RDS database.
* Successfully deployed an Elastic Load Balancer and an Amazon EC2 Auto Scaling Group.
* Set up a practice environment to serve the testing of resource scaling policies.

### Deployment

* Successfully performed the web application deployment on Amazon EC2.
* Created and restored a database from Amazon RDS Snapshots.
* Configured a Target Group, Launch Template, and Application Load Balancer.
* Tested Manual Scaling, Scheduled Scaling, and Dynamic Scaling policies.
* Monitored and evaluated Predictive Scaling via CloudWatch Metrics.

### Skills

* Practiced multi-tier application deployment skills on AWS.
* Practiced configuring Elastic Load Balancer and Amazon EC2 Auto Scaling.
* Improved backup, recovery, and management skills for Amazon RDS databases.
* Formed a workflow of deploying, testing, and cleaning up resources after each lab to optimize costs.