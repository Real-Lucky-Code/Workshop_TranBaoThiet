---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

## Week 6 Goals

* Understand the data backup and recovery mechanism on AWS through AWS Backup.
* Grasp the process of building a Backup Plan, Backup Vault, and managing Recovery Points.
* Learn the monitoring and notification mechanism for the backup process using Amazon SNS.
* Understand the Hybrid Cloud storage model through AWS Storage Gateway combined with Amazon S3.
* Practice deployment, testing, and resource cleanup skills to optimize costs during practice.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| Monday | - Explore an overview of AWS Backup and the lab content.<br>- Prepare the deployment infrastructure.<br>&emsp;+ Create an Amazon S3 Bucket to serve as backup data storage.<br>&emsp;+ Deploy infrastructure using AWS CloudFormation to create an Amazon EC2 Instance, Amazon SNS Topic, and AWS Lambda Function.<br>- Build a Backup Plan.<br>&emsp;+ Create a Backup Vault.<br>&emsp;+ Configure Backup Rules (backup frequency and retention period).<br>&emsp;+ Assign resources to the Backup Plan via Tags or Resource ID. | 25/05/2026 | 25/05/2026 | https://000013.awsstudygroup.com/ |
| Tuesday | - Set up a notification system for AWS Backup.<br>&emsp;+ Configure an Amazon SNS Topic.<br>&emsp;+ Subscribe an email address to receive notifications.<br>&emsp;+ Integrate AWS Backup with Amazon SNS to automatically send notifications when a backup or restore task is completed.<br>- Perform a data recovery capability test.<br>&emsp;+ Check the Recovery Points in the Backup Vault.<br>&emsp;+ Restore resources from a Recovery Point.<br>&emsp;+ Check and confirm the resources operate normally after restoration.<br>- Clean up all resources after completing the lab to avoid incurring costs. | 26/05/2026 | 26/05/2026 | https://000013.awsstudygroup.com/ |
| Wednesday | - Explore an overview of AWS Storage Gateway.<br>- Prepare the Storage Gateway deployment environment.<br>&emsp;+ Create an Amazon S3 Bucket to serve as data storage.<br>&emsp;+ Provision an Amazon EC2 Instance as a Storage Gateway.<br>&emsp;+ Create an EC2 Key Pair and Security Group.<br>&emsp;+ Attach an additional Amazon EBS Volume (150 GiB) as Cache Storage for the Gateway.<br>&emsp;+ Check and record the Public IP of the EC2 Instance to serve Gateway configuration. | 27/05/2026 | 27/05/2026 | https://000024.awsstudygroup.com/ |
| Thursday | - Provision the AWS Storage Gateway.<br>&emsp;+ Connect to the Gateway via the Public IP of the Amazon EC2 Instance.<br>&emsp;+ Configure Cache Storage for the Gateway.<br>- Set up SMB access permissions.<br>- Create a File Share and link it to the Amazon S3 Bucket.<br>- Mount the File Share from an On-premises computer to test access and data synchronization capabilities. | 28/05/2026 | 28/05/2026 | https://000024.awsstudygroup.com/ |
| Friday | - Review and clean up all resources after completing the lab.<br>&emsp;+ Empty the Amazon S3 Bucket.<br>&emsp;+ Delete the AWS Storage Gateway.<br>&emsp;+ Delete the Amazon EC2 Instance and related resources.<br>- Summarize the knowledge learned during the week.<br>- Update the Week 6 Worklog on the reporting.<br>- Plan learning and practice activities for the following week. | 29/05/2026 | 29/05/2026 | https://000024.awsstudygroup.com/3-cleanup/ |

## Week 6 Achievements

### Knowledge

* Understood the data backup and recovery mechanism on AWS through AWS Backup.
* Grasped the process of building a Backup Plan, Backup Vault, and managing Recovery Points.
* Understood the automatic notification mechanism of AWS Backup through Amazon SNS.
* Understood the Hybrid Cloud storage model using AWS Storage Gateway combined with Amazon S3.

### Practice Environment

* Successfully deployed the AWS Backup environment using AWS CloudFormation.
* Configured a Backup Plan and Backup Vault for resources on AWS.
* Successfully set up an Amazon SNS Topic to receive notifications about backup and restore tasks.
* Deployed an AWS Storage Gateway connected to Amazon S3 to serve data storage.

### Deployment

* Successfully performed the resource backup and recovery process using AWS Backup.
* Checked Recovery Points and confirmed data recovery capabilities.
* Created a File Share and connected the AWS Storage Gateway to Amazon S3.
* Mounted the File Share from the On-premises environment and tested data access capabilities.
* Cleaned up all resources after completing the lab to avoid incurring costs.

### Skills

* Practiced skills in building data backup and recovery strategies on AWS.
* Improved skills in configuring Amazon SNS to serve automatic monitoring and notification.
* Practiced deploying the Hybrid Cloud model through AWS Storage Gateway.
* Formed a workflow of deploying, testing, and cleaning up resources after each lab.