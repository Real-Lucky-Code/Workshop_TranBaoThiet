---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

## Week 5 Goals

* Understand the connection mechanism between multiple Amazon VPCs through VPC Peering and AWS Transit Gateway.
* Grasp the process of configuring routing and communication between VPCs within the same Region.
* Understand the role of AWS CloudFormation in automating the infrastructure deployment process.
* Practice configuring, testing, and managing network connections between VPCs on AWS.
* Practice skills in deployment, testing, and resource cleanup to optimize costs during practice.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Explore an overview of AWS CloudFormation and Amazon VPC Peering.<br>- Perform preparation steps for the lab:<br>&emsp;+ Initialize an AWS CloudFormation Template.<br>&emsp;+ Create a Security Group.<br>&emsp;+ Provision Amazon EC2 Instances.<br>&emsp;+ Update Network ACLs to meet connection requirements between VPCs. | 18/05/2026 | 18/05/2026 | https://000019.awsstudygroup.com/ |
| 3 | - Establish an Amazon VPC Peering connection between VPCs.<br>- Configure Route Tables for VPC Peering.<br>- Set up Cross-Peer DNS to support domain name resolution between VPCs.<br>- Test connectivity between Amazon EC2 Instances via VPC Peering.<br>- Clean up all resources of the VPC Peering lab to avoid incurring costs. | 19/05/2026 | 19/05/2026 | https://000019.awsstudygroup.com/ |
| 4 | - Explore an overview of AWS Transit Gateway.<br>- Prepare the deployment environment:<br>&emsp;+ Create an EC2 Key Pair.<br>&emsp;+ Initialize an AWS CloudFormation Template.<br>&emsp;+ Provision an AWS Transit Gateway. | 20/05/2026 | 20/05/2026 | https://000020.awsstudygroup.com/ |
| 5 | - Create Transit Gateway Attachments to connect multiple Amazon VPCs.<br>- Configure Transit Gateway Route Tables.<br>- Test and confirm routing results between VPCs.<br>- Test the communication capability between Amazon EC2 Instances via AWS Transit Gateway. | 21/05/2026 | 21/05/2026 | https://000020.awsstudygroup.com/ |
| 6 | - Clean up all resources of the AWS Transit Gateway lab to avoid incurring costs.<br>- Summarize the knowledge learned during the week.<br>- Update the Week 5 Worklog on the reporting.<br>- Plan learning and practice activities for the following week. | 22/05/2026 | 22/05/2026 | https://000020.awsstudygroup.com/7-cleanup/ |

## Week 5 Achievements

### Knowledge

* Understood the operating principles of Amazon VPC Peering and AWS Transit Gateway.
* Grasped the routing configuration process between multiple Amazon VPCs via Route Tables.
* Understood the domain name resolution mechanism between VPCs using Cross-Peer DNS.
* Understood the role of AWS CloudFormation in automating AWS infrastructure deployment.

### Practice Environment

* Successfully deployed a practice environment using AWS CloudFormation.
* Successfully established an Amazon VPC Peering connection between Amazon VPCs.
* Deployed an AWS Transit Gateway and connected multiple Amazon VPCs via Transit Gateway Attachments.
* Successfully tested the communication capability between Amazon EC2 Instances through network connection models.

### Deployment

* Successfully configured Route Tables for Amazon VPC Peering and AWS Transit Gateway.
* Set up Cross-Peer DNS to serve domain name resolution between Amazon VPCs.
* Tested and confirmed routing results between VPCs.
* Performed cleanup of all resources after completing the lab to avoid incurring costs.

### Skills

* Practiced skills in designing and deploying network connections between multiple Amazon VPCs.
* Practiced using AWS CloudFormation to automate infrastructure deployment.
* Improved skills in configuring Route Tables, Network ACLs, and Transit Gateway.
* Formed a workflow of deploying, testing, and cleaning up resources after each lab.