---
title: "Event 2"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# HARVEST REPORT: AWS COMMUNITY MEETUP (06/06/2026)

### Purpose of the Event

- Explore modern cloud computing technologies on the AWS platform, focusing on critical areas such as system security, containerization, next-generation databases, and real-time application architecture.
- Learn how to combine Machine Learning, Generative AI, and AWS services to build intelligent systems capable of processing complex data and supporting real-world decision-making.
- Gain access to modern Cloud architecture models such as GraphRAG, Serverless Architecture, and Real-time Applications to better understand how enterprises deploy highly scalable systems.
- Learn from the practical experiences of industry experts on career development roadmaps, from foundational positions like IT Helpdesk and System Administrator to specialized roles like Cloud Engineer and DevOps Engineer.
- Enhance awareness of the importance of soft skills, teamwork, communication capabilities, and the spirit of continuous learning in a rapidly changing technology environment.

### Event Information

- **Event Name:** AWS Community Meetup.
- **Program Series:** First Cloud Journey.
- **Time:** June 06, 2026.
- **Format:** Technical Community Event.
- **Participants:** Students, software engineers, Cloud Engineers, DevOps Engineers, AI Engineers, and the AWS technology-loving community.
- **Main Themes:** Cloud Computing, Machine Learning, Generative AI, Containerization, Graph Database, Real-time Architecture, and DevOps.

### List of Speakers

- **Truong Huy Phuoc** - Keynote speaker on the art of effective teamwork.
- **Viet Phat** - AI major student at Swinburne University of Technology.
- **Tran Trung Vinh** - Senior System Administrator at Central Retail Group.
- **Bao Huynh** - Junior Cloud Native Developer at Endava Vietnam, Founder of ITea Lab.
- **Nguyen Quoc Bao** - Keynote speaker on Cloud Multiplayer Game architecture.
- **Le Hoàng Gia Dai** - Final-year student at HUTECH University, member of AWS G3 Team.

### Key Highlights

The AWS Community Meetup focused on many important topics in the modern Cloud ecosystem, ranging from building security infrastructure, deploying containerized applications, developing next-generation AI systems to real-time application architecture.

Instead of just introducing individual AWS services, the speakers focused on analyzing how to combine different technologies to solve real-world business problems. The presented content was not only theoretical but also accompanied by deployment examples, system operation experiences, and practical lessons during product development.

#### Combining Machine Learning with AWS WAF in System Security

One of the prominent topics of the event was the application of Machine Learning to enhance security for Web systems on AWS.

According to the traditional approach, AWS WAF usually operates based on predefined rules (Rule-based / Signature-based), helping detect and prevent common types of attacks such as SQL Injection, Cross-site Scripting (XSS), or predetermined anomalous access behaviors.

However, this method faces limitations when confronting new attacks or previously unseen threats (Zero-day Attacks). Due to the lack of predefined identification information, traditional security systems may face difficulties in detecting anomalous behaviors.

The solution shared in the event was combining Machine Learning with the AWS security system to build a smarter detection mechanism.

Some notable contents:
- Using Machine Learning models like LightGBM to analyze access behavior and identify anomalous patterns.
- Combining multiple AWS services such as VPC, EC2, Application Load Balancer, AWS WAF, Security Hub, GuardDuty, and Amazon Kinesis to build a real-time security monitoring system.
- Transitioning from a reactive security model (Reactive Security) to a model that proactively detects and mitigates risks.

Through this presentation, I realized that modern Cloud security is no longer solely based on fixed rules but requires a combination of automation, data analysis, and artificial intelligence to adapt to emerging threats.

#### Docker and Containerization Technology

Another important content in the event was containerization technology with Docker, one of the popular platforms in software development and deployment processes today.

Before containers, enterprises typically used virtual machines (Virtual Machines) to package applications. However, each virtual machine requires its own operating system, leading to heavy resource consumption and increased deployment time.

Docker solves this problem by packaging the application along with all its dependent libraries into a compact container that can run consistently across multiple different environments.

Some highlights:

- Eliminates the "It works on my machine but not in other environments" problem.
- Packages applications, libraries, and configurations into reusable Docker Images.
- Supports rapid deployment within CI/CD systems.
- Serves as an important foundation for Microservices architecture and Cloud Native Applications.

Through this content, I better understand the role of Docker in the process of modernizing software development workflows, especially when combined with auto-scaling Cloud services.

#### Building Multiplayer Real-time Systems on AWS

Another interesting topic was the architecture for building Multiplayer games on the Cloud platform.

The presentation introduced how to combine the Godot Game Engine with AWS services to build a system capable of real-time communication between multiple players.

The mentioned architecture includes:

- Game Client developed using the Godot Engine.
- AWS API Gateway using WebSockets to maintain a two-way connection between the Client and Server.
- AWS Lambda handling backend logic following the Serverless model.
- Amazon DynamoDB storing player states and game session data.

Some practical issues were also analyzed, such as:

- Handling WebSocket disconnection scenarios (GoneException).
- Cost optimization when the number of players surges.
- Choosing the right architecture between Serverless Architecture and a Dedicated Game Server.

Through this sharing, I better understand how to design systems that require low latency and continuous data synchronization, not only in the gaming field but also in many other real-time applications such as chat, online collaboration, or IoT.

#### Amazon Neptune and GraphRAG in Generative AI Applications

One of the trending topics of the event was the combination of **Generative AI**, **Large Language Models (LLMs)**, and graph databases (**Graph Databases**) to enhance the reasoning capabilities of AI systems.

Previously, applications utilizing the **Retrieval-Augmented Generation (RAG)** model primarily relied on searching for relevant text snippets in the data repository and providing them to the language model to generate answers.

However, for complex problems requiring an understanding of the relationships between multiple distinct entities, the traditional RAG method may face limitations in multi-step reasoning.

The solution introduced in the event was **GraphRAG**, a method that extends RAG by combining a language model with a graph database.

Some notable contents:

- Using **Amazon Neptune** as a Knowledge Graph storage platform, helping represent complex relationships within data.
- Combining with **Amazon Bedrock** to leverage the power of Generative AI models in analysis and response generation.
- Supporting multi-step reasoning (**Multi-hop Reasoning**) by querying relationships within the graph instead of just searching for keywords.
- Can be deployed in multiple directions:
  - Using **Amazon Bedrock Knowledge Bases combined with Neptune Analytics** to simplify the deployment process.
  - Using frameworks like **LlamaIndex** to customize data processing and query workflows.

Through this content, I realize that in enterprise AI systems, data management and context construction play a role just as important as choosing the AI model. A powerful model lacking appropriate data will still struggle to deliver accurate results.

#### Career Development Journey from IT Helpdesk to Cloud Engineer

Alongside technical topics, the event also brought a practical perspective on the career development process in the information technology field.

Through the story of transitioning from an **IT Helpdesk** position to a **Senior System Administrator** and orienting to become a **Cloud/DevOps Engineer**, the speaker shared that career development is not merely based on certifications but must focus on practical competency and problem-solving capabilities.

Some important lessons shared:

- Shift the mindset from traditional server management to managing Cloud infrastructure under the **Pay-as-you-go** model.
- Get familiar with modern tools such as:
  - Infrastructure as Code (Terraform).
  - Continuous Integration / Continuous Deployment (CI/CD).
  - Monitoring and Automation.
- Automating repetitive tasks instead of manual processing.
- Always double-check carefully before modifying Production systems.
- Building personal projects and practical Portfolios instead of strictly focusing on obtaining certifications.

This sharing helped me understand that the growth path in the Cloud industry does not necessarily have to start from a specific position, but what is more important is the capability for continuous learning, accumulating real-world experience, and actively expanding knowledge.

#### The Art of Effective Teamwork in a Technology Environment

In addition to technical content, the event also dedicated an important section to sharing about teamwork skills—a factor that directly impacts the success of technology projects.

The speaker emphasized that an effective team needs not only individuals with professional competencies but also coordination, communication, and shared responsibility capabilities.

Four important principles mentioned include:

##### Defining a Common Goal
Members need to clearly understand the ultimate goal of the project to coordinate and make unified decisions.

##### Assigning the Right Person to the Right Task
Each member should undertake tasks matching their personal strengths to optimize work efficiency.

##### Open Communication
Frequent exchanges, proactive listening, and sharing difficulties help minimize discrepancies during the development process.

##### Emphasizing Personal Responsibility
Each member needs to take responsibility for their portion of the work instead of depending entirely on other members.

Besides, the speaker also introduced several teamwork supporting tools such as:

- Trello.
- ClickUp.
- Google Workspace.
- Slack.
- Discord.

Through this presentation, I noticed that soft skills are an indispensable element for software engineers, particularly in highly complex Cloud and AI projects.

### What I Learned

#### Modern System Design Mindset

Through the sharing sessions at the event, I observed that building a modern technology system does not solely focus on selecting new technologies but requires a comprehensive consideration of scalability, security, cost, and long-term operational capabilities.

Some important lessons:

- Understood the role of the **Container-First** model in building Cloud Native applications, helping the system remain easy to deploy, scale, and maintain across multiple distinct environments.
- Realized the importance of choosing the right data model. For problems requiring the analysis of complex relationships, a Graph Database can deliver far more advantages compared to traditional relational databases.
- Understood that system architecture must be designed based on actual requirements instead of just selecting trendy technologies.

#### Cloud Architecture and System Security

The event helped me better understand how to build Cloud systems with high security and scalability.

Key knowledge includes:

- Understanding how to combine Machine Learning with AWS WAF to build an intelligent security system capable of detecting anomalous behaviors instead of relying strictly on fixed rules.
- Grasping how to deploy real-time applications using WebSockets, Lambda, and DynamoDB.
- Understanding the role of Docker in standardizing deployment environments and supporting CI/CD workflows.
- Realizing the importance of applying Security by Design principles right from the system design phase.

#### Generative AI and Data Management

One of the most crucial pieces of knowledge I acquired was the role of data in AI systems.

Prominent lessons:

- Understood that the quality of an AI system depends not only on the language model but also on how data is organized and context is constructed.
- Understood the difference between traditional RAG and GraphRAG in handling problems requiring multi-step reasoning.
- Realized the potential of Amazon Bedrock and AI services on AWS in building intelligent applications.

#### Career Skills and Teamwork

Alongside technical knowledge, the event also helped me recognize the critical role of soft skills in the career development process.

Some lessons:

- Continuously learning and updating new technologies.
- Actively building personal real-world projects to enhance experience.
- Combining professional skills with communication and teamwork capabilities.
- Understood that a great technology engineer not only solves technical problems but also needs to understand user and business needs.

### Application to Work & Projects

The knowledge absorbed from the AWS Community Meetup can be directly applied to the project development process as well as future career path orientation.

- **Enhance Backend Security:** Applying knowledge of AWS WAF, Machine Learning, and Cloud security architecture to build a better protection layer for the Soccer Field Booking Website's Backend. Methods for detecting anomalous behaviors can be studied to enhance traffic control capabilities and mitigate risk of attacks against the system.
- **Deploy Application Containerization:** Using Docker to package the Java Spring Boot Backend, helping standardize the development and deployment environment. Applying Containers helps minimize the discrepancies between Local, Testing, and Production environments, while creating a favorable foundation when deploying on AWS with models like ECS or Kubernetes in the future.
- **Improve AI Application Capability:** Research applying GraphRAG architecture combined with Amazon Bedrock and Knowledge Bases to develop smarter AI features. Instead of just searching for information based on keywords, the system can exploit relationships within data to deliver highly contextual and more accurate answers.
- **Apply Real-time Architecture When Necessary:** The knowledge regarding WebSockets and the Serverless model grants me additional perspectives in building features that require real-time data updates, such as notifications, field booking statuses, or direct interactions between users.
- **Develop Teamwork Skills:** The principles regarding communication, task division, and progress management shared during the event can be applied to the group project execution process, helping improve coordination efficiency among members.

### Experience During the Event

Participating in the AWS Community Meetup on June 06, 2026, was a valuable experience in the learning process and development orientation within the Cloud Computing field.

#### Accessing Practical Knowledge from Industry Experts:
Listening to direct insights from engineers, Cloud Developers, and people currently working in the AWS field helped me better understand the gap between theoretical knowledge and actual corporate requirements.

#### Expanding Perspectives on Modern System Architecture:
The presentations on AWS WAF, Docker, WebSockets, Amazon Neptune, and GraphRAG helped me understand that building a complete system requires not only choosing the right technology but also considering security, scalability, and operational costs.

#### Better Understanding Technology Industry Development Trends:
Through topics on Generative AI, Machine Learning Security, and Cloud Native Architecture, I observed that AI and Cloud are increasingly tightly combined to create smarter and more automated solutions.

#### Gaining Further Career Development Orientation:
The sharing regarding the journey from IT Helpdesk to Cloud Engineer/DevOps Engineer helped me better understand the skill development roadmap, the importance of building a solid foundation, and accumulating real-world experience.

#### Connecting with the Tech Community:
The event was also an opportunity to exchange and learn from people with similar orientations, thereby expanding knowledge and creating motivation to continue self-developing in the tech field.

### Lessons Learned

Through the AWS Community Meetup event, I realized that becoming a modern software engineer requires not only programming capabilities but also an understanding of system architecture, security, and how to operate applications on the Cloud environment.

Some important lessons:

- **Cloud Security must be designed from the start:** Security should not just be appended after the system is completed but must be considered right during the architectural design process. Combining tools like AWS WAF, Security Hub, and data analysis methods helps the system possess a more proactive defense capability.
- **Mastering foundational technologies is a crucial factor:** Docker, Database Architecture, WebSockets, and AWS services are foundational knowledge pieces that empower engineers with the ability to build modern, highly scalable systems suited for corporate environments.
- **AI in reality needs a combination of model, data, and architecture:** An efficient AI system relies not just on a powerful language model but requires quality data, reasonable information organization, and an output control mechanism.
- **Soft skills play a vital role in the technology environment:** Communication capabilities, teamwork, knowledge sharing, and a continuous self-learning spirit are necessary elements for long-term development in the IT industry.
- **Always maintain a learning and technology-updating mindset:** The Cloud and AI fields change extremely rapidly, so continuously researching, practicing, and building real-world projects is key to enhancing personal capability.

---

### Some Images When Participating in the Event

![Event participation image 1](/images/4-Event/Event2-1.jpg)
![Event participation image 2](/images/4-Event/Event2-2.png)