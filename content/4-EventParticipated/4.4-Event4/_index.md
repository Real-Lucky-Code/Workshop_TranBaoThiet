---
title: "Event 4"
date: 2026-06-27
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Harvest Report: FCAJ COMMUNITY DAY - "DATA DRIVEN, AI RISEN"

### Purpose of the Event

- Update new trends in the fields of Cloud Computing and Generative AI, focusing on deploying AI in enterprise environments.
- Learn about modern AI architectures such as Multi-Agent, Voice AI, AI Agent for DevOps, and Amazon Q to solve real-world problems.
- Enhance understanding of data security solutions when integrating Large Language Models (LLMs) through private network architectures and the Model Context Protocol (MCP).
- Learn practical experiences from experts regarding product development mindset, system performance optimization, and balancing cost, security, and scalability.
- Expand perspectives on AI application trends across various fields such as DevOps, human resource management, customer care, and business process automation.

### Event Information

- **Event name:** FCAJ Community Day - "Data Driven, AI Risen".
- **Program series:** First Cloud AI Journey.
- **Time:** June 27, 2026.
- **Format:** Technical Community Event.
- **Participants:** Students, programmers, AI Engineers, Cloud Engineers, DevOps Engineers, and the AWS technology-loving community.
- **Main themes:** Generative AI, Multi-Agent Systems, Voice AI, DevOps Automation, Amazon Q, AI Security, and Enterprise AI.

### List of Speakers

- **Steve Tran** - CTO/Founder, CloudThinker.
- **Trung Vu** - CEO, Revve AI.
- **Truong Tran** - AI Solution Sales, Noventiq.
- **Anh Dang** - Solution Sales, Noventiq.
- **Nghi Danh** - AI Engineer, Renova Cloud.
- **Kiet Tran** - AI Engineer, AWS Student Builder Group.
- **Bao Phan** - Cloud Engineer, Cloud Kinetics.
- **Nguyen Nguyen** - Cloud Engineer, Cloud Kinetics.
- **Toan Nguyen** - AWS Security Builder.

### Key Highlights

FCAJ Community Day focused on bringing Generative AI models from the research phase into practical deployment within enterprises. The program content not only introduced new technologies but also analyzed practical problems concerning performance, security, cost, and operational capabilities when building large-scale AI systems.

Through the sharing sessions, participants had the opportunity to access multiple modern AI architectures such as Multi-Agent, Voice AI, AI Agent for DevOps, Amazon Q, as well as security solutions tailored for the Enterprise environment.

#### Multi-Agent Architecture and AI Deployment Mindset

Steve Tran opened the program by sharing the mindset of developing AI products towards execution rather than merely focusing on theoretical research.

According to the speaker, in startup projects or MVPs, rapidly building products and continuously improving them based on customer feedback will bring far more value compared to spending too much time perfecting the initial design.

Some highlights:

- Apply the **Champion Customer** strategy to collaborate with enterprises to collect real-world data (Ground Truth).
- Design the system following the **Role-based Multi-Agent** model, where each AI Agent undertakes a specialized task.
- Reduce Hallucination by limiting the processing scope of each individual Agent.
- Focus on optimizing data quality before optimizing the AI model.

Through this presentation, I realized that data quality and architectural design play a much more critical role than simply selecting a powerful AI model.

#### Voice AI and the Vietnamese Language Processing Challenge

A very interesting topic of the event was the Voice AI architecture for enterprises.

A complete Voice AI system consists of three main components:

- Speech-to-Text.
- Large Language Model (LLM).
- Text-to-Speech.

To reduce latency, the system utilizes a **Streaming Response** mechanism, allowing the AI to answer section by section instead of waiting to generate the entire content.

Besides, the speakers also shared the challenges when building Voice AI for the Vietnamese language:

- Vietnamese is a low-resource language with limited training data.
- Difficulty in handling regional intonations and accents.
- Solving **Barge-in** situations, where users interrupt while the AI is responding.

Through this content, I understand that building Voice AI is not just about integrating a language model but also involves optimizing the entire processing pipeline to deliver a natural communication experience.

#### AI Agent in DevOps Automation

Another topic that garnered significant attention was the application of AI Agents into system operations.

AI is utilized to support the entire incident resolution process, including:

- Incident classification.
- Root Cause Analysis (RCA).
- Proposing remediation plans.
- Providing system improvement recommendations.

AI Agents are integrated with monitoring platforms such as Dynatrace to analyze topology, logs, and operational history to determine the cause of errors.

In particular, the speaker emphasized the **Human-in-the-loop** principle, meaning that AI only plays the role of supporting analysis and proposing solutions, while any changes to the Production environment must still be reviewed and approved by humans.

Through this sharing, I better understand the role of AI in modern DevOps, which does not aim to replace operations engineers but helps them make faster and more accurate decisions.

#### Amazon Q in Corporate Governance

The event also introduced how Amazon Q is applied to recruitment and human resource management processes.

Instead of manual resume screening, Amazon Q can:

- Evaluate resumes based on quantitative criteria (Rubrics).
- Understand recruitment requirements based on Instructions.
- Connect directly with HRIS systems.
- Reduce bias during candidate evaluation.

Through this content, I observe that AI serves not only software development but can also automate many business processes in enterprises.

#### Security Architecture with MCP and Private Networking

One of the most crucial topics of the event was data security when deploying AI.

The speakers introduced an architecture utilizing the **Model Context Protocol (MCP)** combined with **PrivateLink** to connect AI models with internal data sources such as SQL Server, Gmail, or Zalo without exposing data to the public Internet.

Some notable contents:

- Establish Private Networking environments for AI.
- Protect enterprise data when utilizing LLMs.
- Balance security and operational costs.
- Apply FinOps in optimizing deployment budgets.

Through this presentation, I notice that security is always a factor that needs to be prioritized when building AI systems for enterprises.

### What I Learned

#### AI System Design Mindset

Through the event, I observe that AI development does not solely focus on language models but requires close attention to data, architecture, and practical deployment capabilities.

Some prominent lessons:

- Prioritize building MVP products and continuously improve based on real-world data.
- Design systems following the Multi-Agent model to enhance accuracy.
- Always center the enterprise's problem when building AI.

#### Cloud Architecture and AI

The event helped me better understand how to deploy AI systems on the AWS platform.

Notable knowledge includes:

- Designing low-latency Voice AI systems.
- Applying AI Agents in DevOps.
- Understanding the role of MCP and PrivateLink in data protection.
- Applying Human-in-the-loop to ensure safety during Production operations.

#### AI Application in Enterprises

Through practical examples, I notice that AI can be applied in various distinct fields.

Important lessons:

- Automate recruitment with Amazon Q.
- Support log analysis and incident resolution.
- Increase operational efficiency through AI Agents.
- Reduce turnaround time and enhance user experience.

### Application to Work & Projects

The knowledge absorbed from FCAJ Community Day can be directly applied to my project development process and future career path orientation.

- **Multi-Agent Application:** Design chatbots to support users following an architecture of multiple specialized Agents to enhance response accuracy.
- **Enhance System Monitoring Capabilities:** Research integrating AI to support log analysis and determine error causes during Backend development.
- **Elevate Data Security:** Apply the Private Networking mindset when designing systems on AWS to restrict unauthorized access and protect user data.
- **Apply Human-in-the-loop:** Design critical functions such as payment or system administration to always include a confirmation step from the administrator before execution.
- **Career Orientation:** The insights from the speakers help me better understand the skills needed to develop toward the orientation of a Backend Developer, Cloud Engineer, or AI Engineer.

### Experience During the Event

Participating in FCAJ Community Day - "Data Driven, AI Risen" brought me many practical perspectives on how enterprises are applying Generative AI and AWS to solve problems in production environments. Not only introducing new technologies, the program also focused on analyzing challenges when deploying AI at an enterprise scale, such as performance, security, cost, and long-term operational capabilities.

#### Accessing AI Problems in Corporate Environments:
The sharing sessions helped me understand that developing AI does not stop at building a language model but requires considering the entire deployment pipeline, from data collection, architectural design, integration with existing systems to post-deployment monitoring and optimization.

#### Expanding Perspectives on Modern AI Architecture:
Through topics like Multi-Agent, Voice AI, Amazon Q, and AI Agents for DevOps, I better understand how to combine multiple AWS services to build scalable, real-time AI systems that meet actual enterprise requirements rather than just stopping at experimental models.

#### Better Understanding Security and Costs in AI Deployment:
One of the contents that left a strong impression on me was using the Model Context Protocol (MCP) combined with PrivateLink to protect data when connecting AI models to internal systems. Through this presentation, I realized that deploying AI in enterprises must always balance performance, security level, and operational costs, while requiring an appropriate FinOps strategy to optimize resources.

#### Recognizing the Role of Humans in AI Systems:
The speakers repeatedly emphasized the Human-in-the-loop principle, where AI supports analysis and proposes solutions, but critical decisions still need to be reviewed and approved by humans. This helps me understand that AI is a tool to support enhancing work efficiency rather than completely replacing the role of engineers or system administrators.

#### Connecting with the Community and Orienting Self-Development:
Alongside professional knowledge, the event was also an opportunity for me to meet experts, Cloud and AI engineers, as well as students with similar orientations. The insights on practical project deployment experiences and career development roadmaps have given me additional motivation to continue learning, researching, and preparing better for work in the Cloud Computing and Generative AI fields.

### Lessons Learned

Through FCAJ Community Day, I observed that building modern AI systems demands a combination of knowledge regarding Cloud Computing, Machine Learning, system architecture, and security.

Some important lessons:

- **Execution is more important than perfection:** Building products rapidly and improving continuously based on real-world data will bring far more value.
- **Multi-Agent helps enhance AI quality:** Dividing tasks among specialized Agents helps reduce Hallucination and increase accuracy.
- **Data security is the top priority:** Enterprise AI systems must be designed with private network architectures and appropriate data protection mechanisms.
- **Humans still hold the deciding role:** AI assists in analysis and proposes solutions, but critical decisions must still be controlled by humans.
- **Continuously learning and updating technology:** Cloud and AI are developing extremely rapidly, so continuous research and practice are essential to elevate professional capacity.

---

### Some Images When Participating in the Event

![Event participation image 1](/images/4-Event/Event4-1.jpg)

![Event participation image 2](/images/4-Event/Event4-2.png)

![Event participation image 3](/images/4-Event/Event4-3.png)