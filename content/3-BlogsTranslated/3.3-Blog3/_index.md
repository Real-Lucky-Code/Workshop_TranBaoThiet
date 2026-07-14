---
title: "Blog 3: How AWS DevOps Agent finds root causes"
date: 2026-04-07
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# HOW AWS DEVOPS AGENT USES MULTI-AGENT REASONING TO FIND ROOT CAUSES

Confirmation bias is one of the most common reasons incident investigations take longer than necessary. An on-call engineer receives an alert, formulates a hypothesis based on experience, finds a matching piece of evidence, and... stops looking. Meanwhile, the actual root cause — which might lie in another service, a different signal, or a different timeframe — remains unresolved.

Modern distributed systems do not lack telemetry data. What they lack is reasoning capability — the ability to generate multiple explanations simultaneously, actively challenge each hypothesis, and draw conclusions only when supported by definitive evidence.

AWS DevOps Agent, an autonomous agent, solves this problem using a multi-agent architecture. It breaks down incident response processes into specialized capabilities. However, what sets this agent apart is not just its ability to search for data, but its understanding of the architectural context — what resources exist, how they are connected, and how they change after each deployment.

This article dives into the incident investigation lifecycle to explore how the AWS DevOps Agent reasons and transforms from a "black box" into a reliable on-call team member.

## 1. The Incident Lifecycle

AWS DevOps Agent organizes the incident response process into specialized capabilities, mirroring the workflows of top-tier SRE (Site Reliability Engineering) teams. All of these share a common foundation:

*   **Triage:** Correlates input signals and enriches the investigation context. Optimized for speed.
*   **Investigation:** Conducts in-depth root cause analysis with parallel hypothesis generation and validation against counter-evidence. This is the core reasoning engine.
*   **Mitigation:** Generates immediate remedial actions based on the identified root cause.
*   **Prevention:** Analyzes patterns from past incidents to prevent future occurrences.

All these capabilities rely on one crucial foundation: the Application Topology graph.

![Figure 1: AWS DevOps Agent Incident Response Lifecycle](/images/3-Blogs/hinh1_blog3.jpg)

## 2. Topology: The Core Foundation

Before it can investigate an incident, the agent needs to understand your architecture — not just as a static list of resources, but as a living map of how they communicate and link back to the source code.

The topology system builds this understanding through:
*   Analyzing AWS CloudFormation (including AWS CDK).
*   Discovering resources via AWS Resource Explorer.
*   Mapping real-time behavior via CloudWatch Application Signals and third-party platforms (Datadog, Dynatrace).
*   Integrating with CI/CD (GitHub Actions, GitLab) to link to the deployment process.

The result is a continuously learning topology structure. When the agent needs to trace an error or assess the blast radius, it relies on this network. Everything operates within an **Agent Space** — an isolated environment scoped to a specific team or application.

![Figure 2: Topology Structure and Agent Space](/images/3-Blogs/hinh2_blog3.jpg)

## 3. Triage: Rapid Categorization and Correlation

When an incident occurs (from CloudWatch, PagerDuty, or Grafana), Triage is the first step triggered. It is optimized for rapidly processing large volumes of data in a short time.

The most critical feature of Triage is **correlation**. The agent automatically links related alarms to determine when they originate from the same event. This minimizes noise and consolidates evidence into a comprehensive investigation. However, ultimate control remains with humans — engineers can easily unlink alerts if they determine they are unrelated.

## 4. Investigation: The Reasoning Engine

This is the centerpiece of the AWS DevOps Agent, following a highly structured methodology.

### Context and Data Gathering
The agent starts with two questions: *What is affected?* and *What recently changed?* It maps the blast radius from the failing resources, checks recent CI/CD deployments, queries metrics and logs from Splunk/Datadog, and analyzes configuration history.

### Hypothesis Generation
Instead of clinging to a single hypothesis, the agent generates multiple competing hypotheses simultaneously:
*   **Pattern matching:** The symptom resembles a past error.
*   **Anomaly detection:** A previously stable metric suddenly deviates.
*   **Temporal correlation:** Deployments or resource constraints (CPU, connection pools) coincide with the incident's onset.

### Evidence Gathering and Root Cause Determination
The agent validates multiple hypotheses in parallel.

**Real-world example:** The checkout service of an e-commerce site experiences increased latency. The agent formulates 3 hypotheses:
1.  There was a configuration change 20 minutes prior.
2.  The payment gateway is responding slowly.
3.  The database connection pool is nearing exhaustion.

Instead of pursuing just one lead, it checks all three: The configuration change only affected logs *(dismissed)*. The payment gateway slowed down *after* the checkout latency spiked -> This is a symptom, not the cause *(dismissed)*. The connection pool hit 94% utilization exactly when the errors began -> **This is the root cause.**

![Figure 3: Parallel Hypothesis Generation and Validation Process](/images/3-Blogs/hinh3_blog3.jpg)

## 5. Mitigation: Safe by Default

After finding the root cause, the agent creates a mitigation plan that includes: A remediation strategy, step-by-step procedures, validation checks, success criteria, and a rollback process.

**Key differentiator:** The AWS DevOps Agent only creates the plan; it *does not automatically execute* actions that modify the system. Its "write" permissions are limited to creating tickets. On-call engineers review the plan, assess the impact via the Topology, and make the final decision. This ensures absolute safety when the system is under high stress.

## 6. Prevention: From Reactive to Proactive

The agent's greatest value lies in connecting the dots between incidents. The Prevention feature groups past incidents that share a common root cause, even if their surface symptoms appear different.

Based on these analyses, the system provides **targeted recommendations** regarding:
*   Observability optimization.
*   Testing and validation.
*   Code resilience patterns, such as retry logic or circuit breakers.
*   Infrastructure optimization and governance standards.

Engineers can add these recommendations to their backlog or reject them using natural language, allowing the AI to learn for future incidents.

![Figure 4: Providing Prevention Recommendations](/images/3-Blogs/hinh4_blog3.jpg)

## 7. Conclusion

The AWS DevOps Agent connects these capabilities into a continuous operational flywheel. The Topology graph provides architectural understanding -> Investigation relies on it to trace errors -> Mitigation uses it to assess risks -> Findings feed back into Prevention to stop recurrences.

By recording its entire reasoning process into an immutable journal and preserving operational knowledge even through personnel changes, the AWS DevOps Agent relieves pressure on on-call engineers, helps them make more accurate decisions, and boosts their confidence whenever a midnight incident strikes.

---
**References:** 
[How AWS DevOps Agent uses multi-agent reasoning to find root causes](https://aws.amazon.com/vi/blogs/devops/how-aws-devops-agent-uses-multi-agent-reasoning-to-find-root-causes/)