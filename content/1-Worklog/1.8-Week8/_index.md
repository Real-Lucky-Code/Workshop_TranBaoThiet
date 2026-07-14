---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

## Week 8 Goals

* Understand the role of the AWS Command Line Interface (AWS CLI) in managing and automating tasks on AWS.
* Install and configure the AWS CLI to connect to an AWS account through Programmatic Access.
* Practice managing common AWS services using the command line, such as Amazon S3, Amazon SNS, IAM, Amazon VPC, and Amazon EC2.
* Familiarize myself with transitioning from operations on the AWS Management Console to managing infrastructure using the Command-Line Interface.
* Develop skills in testing, debugging, and resolving common issues when using the AWS CLI.

## Tasks Implemented During the Week

| Day of Week | Task | Start Date | Completion Date | Reference |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Explore an overview of the AWS Command Line Interface (AWS CLI) and the lab content.<br>- Prepare the environment for using the AWS CLI.<br>&emsp;+ Create an IAM User and grant Programmatic Access.<br>&emsp;+ Attach required access permissions to the IAM User.<br>- Install the AWS CLI on a personal computer.<br>- Configure the AWS CLI using the `aws configure` command, including Access Key ID, Secret Access Key, Default Region, and Output Format. | 08/06/2026 | 08/06/2026 | https://000011.awsstudygroup.com/ |
| 3 | - Practice managing and querying AWS resources using the AWS CLI.<br>- Practice working with Amazon S3.<br>&emsp;+ Create and manage Amazon S3 Buckets.<br>&emsp;+ Upload and Download Objects.<br>&emsp;+ Synchronize data using the `aws s3 sync` command.<br>- Practice working with Amazon SNS.<br>&emsp;+ Create an Amazon SNS Topic.<br>&emsp;+ Set up Subscriptions.<br>&emsp;+ Publish Messages to test SNS operations. | 09/06/2026 | 09/06/2026 | https://000011.awsstudygroup.com/ |
| 4 | - Practice managing IAM using the AWS CLI.<br>&emsp;+ Create IAM Users and IAM Groups.<br>&emsp;+ Add IAM Users to Groups.<br>&emsp;+ Attach IAM Policies.<br>&emsp;+ Create Access Keys for IAM Users.<br>- Practice managing network infrastructure using the AWS CLI.<br>&emsp;+ Create an Amazon VPC.<br>&emsp;+ Create Subnets and Route Tables.<br>&emsp;+ Create an Internet Gateway and attach it to the Amazon VPC to establish an Internet connection. | 10/06/2026 | 10/06/2026 | https://000011.awsstudygroup.com/ |
| 5 | - Initialize an Amazon EC2 Instance using the AWS CLI.<br>&emsp;+ Create an EC2 Key Pair and Security Group.<br>&emsp;+ Launch an Amazon EC2 Instance using the `aws ec2 run-instances` command with parameters such as Amazon Machine Image (AMI), Instance Type, and Subnet ID.<br>&emsp;+ Check the operating status using the `aws ec2 describe-instances` command.<br>- Practice Troubleshooting.<br>&emsp;+ Check and resolve errors regarding Credentials, IAM Permissions, and Regions.<br>&emsp;+ Use the `--debug` parameter to analyze logs and support troubleshooting. | 11/06/2026 | 11/06/2026 | https://000011.awsstudygroup.com/<br/>https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-troubleshooting.html |
| 6 | - Review and clean up all created resources using the AWS CLI to avoid incurring costs.<br>- Summarize the knowledge learned during the week.<br>- Update the Week 8 Worklog on the reporting.<br>- Plan learning and practice activities for the following week. | 12/06/2026 | 12/06/2026 | https://000011.awsstudygroup.com/11-cleanup/ |

## Week 8 Achievements

### Knowledge

* Understood the role of the AWS Command Line Interface (AWS CLI) in managing and automating tasks on AWS.
* Grasped the process of installing, configuring, and authenticating the AWS CLI through IAM Users and Programmatic Access.
* Understood how to manage common AWS services such as Amazon S3, Amazon SNS, IAM, Amazon VPC, and Amazon EC2 using the command line.
* Understood the process of testing and resolving common errors when using the AWS CLI.

### Practice Environment

* Successfully installed and configured the AWS CLI on a personal computer.
* Set up an IAM User and Programmatic Access to use the AWS CLI.
* Practiced managing AWS resources through the Command-Line Interface instead of the AWS Management Console.
* Completed the environment to serve the automation of administrative tasks on AWS.

### Deployment

* Successfully performed management operations on Amazon S3, Amazon SNS, IAM, Amazon VPC, and Amazon EC2 using the AWS CLI.
* Provisioned and managed an Amazon EC2 Instance through AWS CLI commands.
* Performed queries, verifications, and management of AWS resources using CLI commands.
* Applied Troubleshooting techniques to handle errors related to Credentials, IAM Permissions, and Regions.
* Cleaned up all resources after completing the lab to avoid incurring costs.

### Skills

* Practiced skills in managing AWS infrastructure using the Command-Line Interface.
* Improved skills in using the AWS CLI to automate administrative tasks on AWS.
* Practiced testing, analyzing logs, and troubleshooting using the `--debug` parameter.
* Formed a workflow of deploying, testing, and cleaning up resources according to best practices on AWS.