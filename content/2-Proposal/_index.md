---
title: "Proposal"
date: 2026-07-04
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Sports Field Booking Website Project
## AWS High Availability & Scalable Architecture Deployment Solution
### 1. Executive Summary
The Sports Field Booking System is designed to provide a stable, secure, and highly available web platform for users. The platform utilizes an AWS architecture with a complete separation of Frontend (static) and Backend (dynamic), leveraging Auto Scaling capabilities spanning across multiple Availability Zones (Multi-AZ). This solution ensures the system always operates smoothly even during peak hours, optimizing operational costs and ensuring data safety with Amazon RDS and in-depth security layers such as AWS WAF.

### 2. Problem Statement
### Current Issues
Traditional sports field booking systems often experience overload, slow responses, or website crashes during peak hours (e.g., 5:00 PM - 7:00 PM). Centralized storage on a single server (Single Point of Failure) poses a risk of data loss, while the cost of maintaining high-configuration servers 24/7 wastes the budget when system traffic is low.

### Solution
The project applies a Cloud-native architecture on AWS. The Frontend is stored statically on Amazon S3 and distributed with ultra-high speed via CloudFront. Directly handling the Backend logic is a cluster of EC2 servers (using Java Spring Boot) located in Private Subnets, with load managed by an Application Load Balancer (ALB) and an Auto Scaling Group. The MySQL database is hosted on Amazon RDS following the Multi-AZ model (with a standby backup copy) for fault tolerance. The system is also continuously monitored by CloudWatch and alerted via SNS.

Benefits and Return on Investment (ROI)
This architecture delivers an uptime of up to 99.9%, enhancing the booking experience for end-users. The system only scales out computing resources when there is high traffic and scales in when idle, maximizing infrastructure cost savings. Additionally, maintenance and upgrades occur seamlessly thanks to the distributed architecture, causing no service disruption.

### 3. Solution Architecture
The platform applies an AWS architecture combining Serverless (for Frontend/Storage) and Auto-scaling Instances (for Backend/Database) across 2 Availability Zones (AZ A and AZ B).

### Data Flow:
![Sports field booking website project](/images/2-Proposal/anh_kien_truc.png)

- **Access & Security (1)**: Users access the domain name resolved by Route 53. Traffic passes through CloudFront (CDN) and is inspected for security by AWS WAF.

- **Frontend (3)**: CloudFront fetches static interface data (ReactJS/Vue/HTML...) from the FE Static S3 bucket.

- **Backend Routing (2, 4)**: API requests pass through the Internet Gateway (IGW) to the Internet-facing ALB. The ALB distributes the load to the Target Group.

- **Logic Processing (5)**: The Target Group routes requests to EC2 instances located within the Auto Scaling Group in the Private Subnets of AZ A or AZ B. These servers use a NAT Gateway in the Public Subnets to access the Internet when necessary (e.g., calling third-party payment APIs).

- **Database (6)**: EC2 connects to the Amazon RDS MySQL (Primary) via the RDS Endpoint and Security Groups. Data is continuously synchronized to the Standby copy in AZ B (Multi-AZ) to ensure safety and high availability.

- **Backend Static Storage (7)**: Files uploaded by users (field images, invoices, avatars) are pushed by EC2 into the BE S3 bucket through an S3 Gateway Endpoint.

- **Monitoring & Alerting (8)**: The status of the RDS and the system is collected by CloudWatch; if an incident occurs, it triggers AWS SNS to send warning emails to administrators.

### Main AWS Services Used

- **Amazon Route 53, CloudFront & WAF**: Manage DNS, accelerate page loading speed, and protect the system from common web attacks (such as DDoS, SQL Injection).

- **Application Load Balancer (ALB) & Auto Scaling Group**: Balance load and automatically scale out/in the number of EC2 servers.

- **Amazon EC2**: Run the Backend application (Java Spring Boot, Hibernate).

- **Amazon RDS (MySQL, Multi-AZ)**: Manage the relational database, automatically failing over when an incident occurs.

- **Amazon VPC, NAT Gateway, IGW**: Build a virtual private network, separating Public and Private environments for absolute security of the Backend and DB.

- **Amazon S3**: Store the static Frontend (FE Static S3) and system files (BE S3).

- **Amazon CloudWatch & SNS**: Monitor resources, logs, and automatically notify via Email.

### 4. Technical Implementation
### Deployment Phases
**The project is divided into 4 main phases to bring the application onto AWS:**

- **Basic Network & Storage Setup**: Configure the VPC, divide Subnets (Public/Private), set up the IGW, NAT Gateway, and S3 buckets. Push static Frontend code to S3.

- **Database & Server Configuration**: Initialize Amazon RDS MySQL (Multi-AZ). Configure the Launch Template for EC2 containing the Java/Node.js runtime environment, and set up the Auto Scaling Group and ALB.

- **Edge Network & Security Deployment**: Connect Route 53 with the domain name, configure CloudFront to distribute Frontend S3, and attach AWS WAF to protect the ALB/CloudFront.

- **Monitoring & Optimization**: Set up monitoring metrics on CloudWatch, configure SNS to send emails when EC2 is overloaded or RDS encounters errors. Configure CI/CD to automatically deploy new code.

### Technical Requirements

- **Frontend**: Built into static files (HTML/CSS/JS) optimized for S3 static website hosting.

- **Backend**: The application (e.g., Java Spring Boot) must follow the Stateless standard (no sessions stored on the server, using JWT) for Auto Scaling to function correctly. Run via port 80/8080 for ALB health checks.

- **Database**: Use MySQL with Hibernate/JPA connection, configuring an optimized connection pool to handle the load from multiple EC2 instances simultaneously.

### 5. Roadmap & Implementation Milestones
- **Week 1**: Local Finalization & Infrastructure Initialization

    - Complete programming and functional testing of the Sports Field Booking system (static interface and Java Spring Boot backend) in the local environment.
    - Create an AWS account, design the core network (VPC, Public/Private Subnets, Internet Gateway).

- **Week 2**: Data & Edge Network Deployment

    - Initialize and configure the MySQL database on Amazon RDS.

    - Upload static Frontend source code to the S3 bucket and configure high-speed content distribution via CloudFront.

- **Week 3**: Backend Deployment & Auto Scaling

    - Package the Backend application, create a Launch Template, and set up the EC2 Auto Scaling server cluster.

    - Configure the Application Load Balancer (ALB) to route traffic securely into the Backend.

- **Week 4**: Finalization, Testing & Reporting

    - Integrate the actual domain name (Route 53) and set up system monitoring and alerting via CloudWatch combined with SNS.

    - Perform load testing, review cost optimization, and complete the project report book.

### 6. Budget Estimation
You can view the budget estimation table on the [AWS Pricing Calculator](https://calculator.aws/#/estimate?id=621f38b12a1ef026842ba2ddfe46ff936ed4ab01).  
Alternatively, you can download the [Budget Estimation File](../attachments/budget_estimation.pdf).

**Infrastructure Costs (Estimated)**

 - Application Load Balancer (ALB): ~16.50 USD/month.

 - Amazon EC2 (2 t3.micro instances in Auto Scaling): ~15.00 USD/month.

 - Amazon RDS (MySQL t3.micro, Multi-AZ): ~34.00 USD/month.

 - NAT Gateway (1 unit): ~32.00 USD/month.

 - Amazon S3 & CloudFront (Low traffic): ~2.00 USD/month.

 - Route 53 (1 Hosted Zone): 0.50 USD/month.

 - AWS WAF, CloudWatch, SNS: Within Free Tier or ~3.00 USD/month.

Total: Approximately 103.00 USD/month.

### 7. Risk Assessment
**Risk Matrix**

 - DDoS attack or Web Exploit: High impact, medium probability.

 - Database overload due to complex queries: High impact, high probability (if there is a spike in field bookings).

 - Exceeding AWS budget (Cloud Shock): High impact, medium probability.

 - Mitigation Strategies

 - Security: Use AWS WAF to block malicious IPs, Rate Limiting on CloudFront/ALB. Place the DB and Backend in Private Subnets without assigning public IPs.

 - Database: Leverage Read Replicas (if read scaling is needed), optimize MySQL indexes, use Hibernate Caching.

 - Cost: Set up AWS Budgets to alert immediately if costs exceed thresholds of $10, $20. Turn off EC2 instances and RDS at night when not developing.

### 8. Expected Outcomes

**Technically**

- The system operates stably on AWS.
- Capable of scaling when traffic increases.
- Ensures high availability and data safety.
- Optimizes performance and operational costs.

**Academically**

- Through the project, I have the opportunity to apply knowledge of AWS Cloud, Java Spring Boot, and actual system deployment in a corporate environment. This will serve as an important foundation for developing toward the orientation of a Backend Developer, Cloud Engineer, or DevOps Engineer in the future.