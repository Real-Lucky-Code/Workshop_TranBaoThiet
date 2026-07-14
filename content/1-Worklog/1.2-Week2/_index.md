---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

## Week 2 Goals

* Understand the identity and access management mechanism on AWS through the AWS Identity and Access Management (IAM) service.
* Grasp foundational knowledge of Amazon VPC and network infrastructure components on AWS.
* Deploy and manage Amazon EC2 in a VPC environment.
* Learn the operating principles and configuration process of Site-to-Site VPN connections on AWS.
* Practice skills in deployment, connection testing, and resource cleanup to optimize costs during practice.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Explore an overview of the AWS Identity and Access Management (IAM) service.<br>- Study the main components including: IAM Users, IAM Groups, IAM Policies, and IAM Roles.<br>- Practice creating an Admin Group and Admin User.<br>- Create an Admin Role and OperatorUser.<br>- Configure and perform Switch Role to test permissions.<br>- Clean up resources after completing the lab. | 27/04/2026 | 27/04/2026 | https://000002.awsstudygroup.com/ |
| 3 | - Explore an overview of Amazon VPC and network security components.<br>- Perform network infrastructure preparation steps:<br>&emsp;+ Create a VPC.<br>&emsp;+ Create a Public Subnet and Private Subnet.<br>&emsp;+ Create an Internet Gateway.<br>&emsp;+ Configure Route Tables.<br>&emsp;+ Create Security Groups.<br>&emsp;+ Enable VPC Flow Logs. | 28/04/2026 | 28/04/2026 | https://000003.awsstudygroup.com/ |
| 4 | - Deploy an Amazon EC2 Instance in the VPC.<br>- Test connectivity to the EC2 Instance.<br>- Create a NAT Gateway.<br>- Use Reachability Analyzer to test network flow.<br>- Create an EC2 Instance Connect Endpoint.<br>- Manage EC2 via AWS Systems Manager Session Manager.<br>- Set up CloudWatch Monitoring and Alerting. | 29/04/2026 | 29/04/2026 | https://000003.awsstudygroup.com/4-createec2server/ |
| 5 | - Learn about and deploy an AWS Site-to-Site VPN connection.<br>- Prepare the VPN environment:<br>&emsp;+ Create a VPC for the VPN.<br>&emsp;+ Create an EC2 instance as the Customer Gateway.<br>- Configure a Virtual Private Gateway, Customer Gateway, and VPN Connection.<br>- Configure the Customer Gateway and customize the AWS VPN Tunnel.<br>- Explore alternative VPN options and the VPN Troubleshooting Guide. | 30/04/2026 | 30/04/2026 | https://000003.awsstudygroup.com/5-vpnsitetosite/ |
| 6 | - Review and clean up all created resources to avoid incurring costs.<br>- Summarize the knowledge learned during the week.<br>- Update the Week 2 Worklog on the reporting.<br>- Plan learning and practice activities for the following week. | 01/05/2026 | 01/05/2026 | https://000003.awsstudygroup.com/6-cleanup/ |

## Week 2 Achievements

### Knowledge

* Understood the identity and access management mechanism on AWS through the IAM service.
* Grasped the roles and usage of IAM Users, IAM Groups, IAM Policies, and IAM Roles.
* Understood the basic network architecture of Amazon VPC and the functions of components such as VPCs, Subnets, Internet Gateways, Route Tables, and Security Groups.
* Understood the operating principles of NAT Gateway, Reachability Analyzer, and Site-to-Site VPN in connecting and managing network infrastructure on AWS.

### Practice Environment

* Successfully deployed a basic network environment on AWS with Amazon VPC.
* Provisioned and managed an Amazon EC2 Instance in a VPC environment.
* Set up and used AWS Systems Manager Session Manager to manage EC2.
* Set up CloudWatch Monitoring and Alerting to monitor resources.

### Deployment and Security

* Created and managed IAM Users, IAM Groups, and IAM Roles.
* Configured and tested the Switch Role mechanism to verify access permissions.
* Deployed a basic Site-to-Site VPN environment between AWS and a simulated Customer Gateway system.
* Understood the VPN Tunnel configuration process and basic troubleshooting methods.

### Skills

* Practiced skills in designing and deploying basic network infrastructure on AWS.
* Practiced testing connections and analyzing network flow using Reachability Analyzer.
* Formed a workflow of deploying, testing, and cleaning up resources after each lab to optimize costs.
* Improved self-learning capabilities through the program's instructional materials and lab exercises.