---
title: "Event 1"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Harvest Report: "AWS First Cloud AI Journey – Community Day"

### Purpose of the Event

- Update the latest technology trends in the fields of **Cloud Computing**, **Generative AI (GenAI)**, and **Large Language Models (LLMs)** through presentations by experts currently working in enterprises.
- Share practical experiences in designing, deploying, and operating AI systems as well as Cloud infrastructure in a modern, secure, and cost-optimized direction.
- Introduce AI application solutions for enterprises such as **Agentic AI**, **Multi-Agent Systems**, **GenAIOps**, and AWS services serving the product development process.
- Create opportunities for the technology community to network, exchange experiences, and learn from real-world case studies in various fields such as finance, banking, DevOps, and software development.
- Orient the mindset of building AI systems capable of scaling, controlling risks, and bringing real value to enterprises.

### Event Information

- **Event name:** AWS First Cloud AI Journey – Community Day.
- **Program series:** First Cloud Journey.
- **Time:** May 23, 2026.
- **Format:** Technical Community Event.
- **Participants:** Students, software engineers, DevOps Engineers, AI Engineers, and the community that loves AWS technology.
- **Main themes:** Cloud Computing, Generative AI, Large Language Models, Multi-Agent Systems, and AWS services.

### List of Speakers

The event gathered many experts working at large enterprises and technology organizations, bringing multi-dimensional perspectives from software development, DevOps to AI architecture and Cloud infrastructure.

- **Tinh Truong** – Platform Engineer, GoTymeX.
- **Pham Nguyen Hai Anh** – AWS Community Builder, G-AsiaPacific Vietnam.
- **Nguyen Tuan Thinh** – DevOps Engineer, First Cloud AI Journey.
- **Team VIB (Thao Nguyen, Mai Nguyen, Uyen Lee)** – Authors of the **UTMorpho** project, champion of LotusHacks 2026.
- **Duc Dao** – Solutions Architect, Cloud Kinetics.
- **Vy Lam** – Senior Business Systems Analyst, VPBank.

### Key Highlights

The program was built around two prominent technology trends today: **Cloud Infrastructure** and **Generative AI**. Instead of just introducing individual AWS services, the speakers focused on how to combine multiple technologies to solve real-world problems in enterprises, from developing AI products and optimizing Cloud infrastructure to building large-scale Multi-Agent systems.

The highlight of the event was that all content was illustrated with real-world projects, enterprise case studies, and deployment experiences from the speakers themselves. As a result, participants not only understood how a technology works but also knew when to apply it, the benefits it brings, as well as the challenges to consider when deploying in a real environment.

#### AI Application in Product Development

One of the opening topics of the event was the development journey of **UTMorpho** – a project that achieved high marks at the **LotusHacks 2026** competition. Through the development team's real story, the speaker shared the process of turning an initial idea into a complete product in just **36 hours**, from defining the problem and designing the solution to building and demonstrating the product.

The highlight of UTMorpho is that it solves the limitations of traditional UI-generating AI tools. Instead of having to re-prompt the entire command every time they want to edit the interface, users can interact directly on the interface (WYSIWYG) and only change the exact component desired.

Some highlights of the solution include:

- Supports direct editing on the interface without regenerating the entire layout.
- Applies the **Scoped Edit** mechanism to only update the selected region, keeping the remaining components intact.
- Uses **Smart Diffing** to reduce the number of tokens to be processed, thereby optimizing costs when using AI models.
- Possesses the capability to quickly generate **React** source code from descriptions in natural language.

Besides the technical aspect, the presentation also emphasized that a successful product comes not only from technology but also from teamwork, reasonable division of labor, and focusing on solving the exact needs of users.


#### Agentic AI and Enterprise Process Automation

Another prominent topic was the **Agentic AI** trend, in which AI not only assists in answering questions but also has the capability to actively execute multiple consecutive tasks to complete a specific goal.

The speaker introduced the **Amazon Quick Suite** ecosystem, which allows connecting various data sources such as databases, internal documents, websites, and user-provided files to build AI assistants for enterprises.

Notable capabilities include:

- Automatically summarize and analyze information from multiple data sources.
- Generate Meeting Minutes after a meeting ends.
- Automatically send emails to relevant members.
- Support scheduling subsequent meetings.
- Build Dashboards and reports using natural language without programming.
- Increase knowledge sharing and management capabilities within the organization through a shared workspace.

Through this presentation, I realized that AI is gradually transitioning from a personal assistant role to becoming a "digital colleague", capable of automating many processes in enterprises and helping shorten the time from having data to making decisions.


#### Amazon CloudFront – Platform for System Acceleration and Protection

Alongside AI topics, the event also dedicated a significant amount of time to share about **Amazon CloudFront** and the role of this service in building modern Cloud infrastructure.

Instead of just viewing CloudFront as a CDN service, the speaker analyzed CloudFront as the first layer of protection between users and the backend system, while playing an important role in optimizing performance, costs, and security capabilities.

Some notable contents include:

- Accelerate access by distributing content through a global network of Edge Locations.
- Reduce load on the origin server (Origin) through Caching and HTTP Compression.
- Reduce data transfer costs between AWS services.
- Support a fixed pricing mechanism (Flat-rate Pricing), helping enterprises forecast costs more easily.
- Block DDoS attacks right at the Edge before traffic reaches the backend system.
- Support Mutual TLS (mTLS) to enhance security for systems requiring two-way authentication.
- Completely hide the underlying infrastructure using solutions like **Origin Access Control (OAC)** and **VPC Origin**, restricting direct access to servers.

Through real-world examples, the speaker demonstrated that deploying CloudFront not only helps improve performance but also contributes to significantly reducing operational costs and enhancing the security capability of the entire system.


#### Enterprise Multi-Agent Systems

One of the most impressive presentations was the **Multi-Agent System** model applied to the credit scoring problem for startup enterprises.

The speaker pointed out that AI systems using a single Agent often face many limitations when handling complex business logic. When the data volume is large and spread across multiple fields, it is difficult for a single Agent to simultaneously undertake all tasks with high accuracy.

The introduced solution is to build multiple specialized Agents, each undertaking a distinct role such as:

- Financial analysis.
- Market evaluation.
- Founding team capability appraisal.
- Risk assessment.
- Legal compliance verification.

The entire process is coordinated by a **Manager Agent**, playing the role of summarizing results and making the final decision.

This model helps increase specialization, reduce errors in the evaluation process, enhance the scalability of AI systems, and demonstrates wide application potential in the fields of finance, banking, and enterprises.


#### Context Is Everything

A consistent message throughout the event was **"Context is Everything"**. According to the speaker, the quality of AI results does not depend entirely on the model but depends heavily on the quality of the context (Context) provided.

The presentation pointed out many common mistakes when using AI, such as:

- Providing too many irrelevant documents, making it difficult for the AI to identify important information.
- Giving overly general requests that lack specific goals.
- Failing to clearly describe constraints or criteria for evaluating results.

To solve this problem, the speaker proposed a context management workflow consisting of:

- **Store:** Store knowledge.
- **Retrieve:** Retrieve exactly the necessary information.
- **Generate:** Generate content based on the appropriate context.
- **Learn:** Memorize to improve subsequent interactions.

Through the presentation, I realized that designing an effective Context is just as important as selecting the AI model, and it serves as the foundation for helping Generative AI systems operate accurately, stably, and deliver practical value.


#### Correctly Understanding the Non-determinism of Large Language Models

The final topic focused on a very practical problem when working with large language models: **non-determinism (Non-determinism)**.

The speaker analyzed that many people often assume setting **Temperature = 0** will always produce the exact same result. However, in reality, this is not entirely true.

Some explained causes include:

- Floating-point calculation errors on the GPU.
- Parallel processing mechanisms of the hardware.
- Inference Batching techniques by AI service providers.

To reduce the impact of this phenomenon, the speaker proposed several solutions such as:

- Running multiple times and selecting the most appropriate result.
- Using **JSON Mode** or **Function Calling** to standardize the output.
- Designing a processing layer to validate data before it enters the system.
- Adjusting the Temperature to an appropriate level instead of always setting it to 0.

The sharing helped me understand that developing AI applications does not stop at Prompt Engineering but also requires attention to how to control, evaluate, and ensure the output quality of the model during actual operations.

### What I Learned

#### AI Mindset

- Understood that the quality of a **Generative AI** system does not rely solely on the Large Language Model (LLM) but depends heavily on the provided **Context**. Constructing an appropriate context helps the AI generate accurate, consistent responses and reduces Hallucination.
- Clearly recognized the role of **Context Engineering** in designing modern AI applications, ranging from data organization and knowledge management to model cost optimization.
- Understood the benefits of **Agentic AI** and **Multi-Agent Systems** architectures, where specialized agents collaborate to solve complex problems instead of assigning the entire workload to a single model.
- Realized that deploying AI in enterprises needs to be evaluated based on the practical value it delivers—such as productivity, turnaround time, operational costs, and scalability—rather than just focusing on the technology itself.

#### Cloud Infrastructure Design Mindset

- Understood that performance optimization does not only take place at the Backend server level but must be implemented right from the **Edge** layer, where users begin accessing the system.
- Grasped the role of **Amazon CloudFront** in accelerating access, reducing the load on the origin server (Origin), while enhancing security capabilities and optimizing operational costs.
- Understood how to balance **performance, security, scalability, and cost** when designing Cloud architectures, rather than focusing solely on a single isolated factor.

#### Technical Knowledge

- Better understood the **Non-determinism** nature of Large Language Models and why the exact same Prompt can still generate different results.
- Learned how to improve output stability through techniques such as **JSON Mode**, **Function Calling**, **Majority Voting**, and selecting appropriate parameters.
- Understood the role of **GenAIOps** in managing the lifecycle of AI systems, from building and deployment to monitoring and optimization during actual operations.

#### Skills and Practical Perspectives

- Learned how to approach problems from an enterprise perspective, where technology is merely a tool to solve practical needs and create value.
- Better understood the process of developing an AI product from inception, design, and testing to deployment in a real-world environment.
- Expanded the mindset on how to evaluate a solution based on the efficiency it brings, its deployability, and sustainability, rather than relying strictly on how modern the technology is.
- Noticed the importance of continuously updating knowledge regarding Cloud Computing and Generative AI to adapt to rapid shifts in technology and enterprise demands.

### Application to Work

The knowledge gained from the event can be directly applied to the learning process, project execution, as well as future Cloud projects.

Some application orientations include:

- Applying **Amazon CloudFront** combined with **Origin Access Control (OAC)** to accelerate access, protect backend systems, and restrict direct access to servers in projects deployed on AWS.
- Utilizing **Context Engineering** principles when building chatbots or applications that use Large Language Models to enhance response quality and minimize Hallucination.
- Designing AI systems towards a **Multi-Agent** approach, breaking down tasks into multiple specialized components to improve scalability and maintainability.
- Applying AI output standardization techniques like **JSON Mode** or **Function Calling** to increase stability when integrating with software systems.
- Referencing experiences regarding cost, performance, and security optimization when designing Cloud architectures, particularly in projects deployed on the AWS platform.
- Continuing to research and practice emerging technologies such as Agentic AI, GenAIOps, and Amazon Bedrock to elevate professional knowledge as well as prepare for future AWS certifications.

### Experience During the Event

Participating in the **AWS First Cloud AI Journey – Community Day** event was a highly meaningful experience that granted me access to many new technology trends and allowed me to learn various practical experiences from industry experts.

#### Accessing New Technology Trends

- Updated on prominent trends in Generative AI, Agentic AI, Multi-Agent Systems, and GenAIOps that draw significant interest from enterprises.
- Better understood how organizations apply AI in combination with the AWS platform to solve real-world problems in finance, banking, and software development.
- Expanded the perspective on how AI and Cloud Computing are supporting enterprises in improving operational efficiency and optimizing costs.

#### Learning from Experts and Real-World Scenarios

- The presentations all originated from projects deployed in reality, which helped me better understand the hurdles and experiences when introducing AI into corporate environments.
- Observed multiple illustrations, product demonstrations, and real case studies, making it easier to visualize how to apply this knowledge to future projects.
- Understood that choosing the right solution is always more important than using the latest technology.

#### Expanding the Mindset on Product Development

- The journey of developing UTMorpho within the framework of the Hackathon competition helped me better understand the product-building process from concept to deployment in a short span of time.
- The insights on Context Engineering and Multi-Agent Systems helped reshape my approach to building AI applications, moving towards designing more scalable and maintainability-friendly systems.
- The content regarding CloudFront and infrastructure optimization also provided me with numerous ideas for designing secure and efficient Cloud systems.

#### Networking and Exchange

- The event created opportunities to network with experts, engineers, and the AWS-loving community, thereby gaining diverse experiences and distinct perspectives in the software development process.
- Discussion and Q&A sessions helped clarify common issues encountered when deploying AI and Cloud in enterprise environments.

#### Lessons Learned

Through the AWS First Cloud AI Journey – Community Day event, I realized that deploying Cloud and AI solutions in enterprises depends not only on technology but also demands system design thinking, the ability to choose an appropriate architecture, and evaluating efficiency based on actual needs.

The presentations provided a clearer understanding that building AI applications requires paying close attention to context quality (Context), model output control mechanisms, and the coordination among multiple AI Agents to solve complex problems. At the same time, modern Cloud infrastructure must also be designed with performance, security, and cost optimization in mind right from the initial phase.

In addition to professional knowledge, the event delivered extensive practical experience regarding product development, teamwork, and project deployment in corporate environments. These are valuable lessons that will guide me more clearly through my future studies, research, and development of Cloud and AI projects.

### Conclusion

AWS First Cloud AI Journey – Community Day not only brought updated knowledge on Cloud Computing and Generative AI but also helped me better understand how enterprises are applying these technologies to solve real-world problems.

Through the presentations, I had the opportunity to access modern architectural models such as Agentic AI, Multi-Agent Systems, GenAIOps, and infrastructure solutions on AWS. Simultaneously, I became more aware that building an efficient system relies not just on technology but requires balancing performance, security, scalability, cost, and the value brought to the enterprise.

The knowledge and experience gathered from the event will serve as a useful foundation for me to continue learning, researching, and applying to future theses, personal projects, as well as my career development path in Cloud Computing and Artificial Intelligence.

---

### Some Images When Participating in the Event

![Event participation image 1](/images/4-Event/Event1-1.jpg)
![Event participation image 2](/images/4-Event/Event1-2.png)