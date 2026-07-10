---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---




# Reflection Report: “THE HIDDEN ICEBERG OF A PROJECT: DEVOPS BEFORE DISASTER”

### Event Objectives

- Identify hidden risks (the submerged part of the iceberg) in the software development lifecycle.
- Introduce practical DevOps methodologies and culture to prevent project disasters.
- Guide the building of an automation mindset (CI/CD, IaC) and proactive system monitoring.
- Bridge the gap between the Development and Operations teams.

### Speaker List

- **[Speaker Name]** - Tran Minh Quan

### Key Highlights

#### The Iceberg Metaphor in Projects

- **The Tip (Visible part):** User Interface (UI), new features, release speed.
- **The Submerged Part (Hidden risks):** Technical debt, security vulnerabilities, manual deployment processes, lack of monitoring mechanisms, missing system documentation.
- **Consequences:** System crashes during peak hours, data loss, wasting time fixing bugs (firefighting) instead of developing new features.

#### Mindset Shift: From "Firefighting" to "Prevention" with DevOps

Solving the submerged issues using the core pillars of DevOps:
- **Continuous Integration (CI):** Continuous integration, detecting bugs early (shift-left testing) right from the coding phase.
- **Continuous Deployment/Delivery (CD):** Automating the pipeline to deploy products to the production environment, ensuring safety and fast rollback capabilities.
- **Infrastructure as Code (IaC):** Managing and provisioning infrastructure through code, eliminating human errors from manual operations.

#### Risk Management and Proactive Monitoring (Observability)

- **The Difference between Monitoring and Observability:** Not just seeing if the system is alive or dead, but understanding *why* it has issues.
- **The 3 Pillars of Observability:** Logs, Metrics, and Traces.
- **Alerting:** Detecting incidents and sending notifications before users even notice and complain.

#### Breaking Down Silos (Culture & Collaboration)

- DevOps is not a job title or a tool, it is a **culture**.
- **Shared Responsibility:** Devs need to care about how their code runs on the server, and Ops needs to understand the flow of the code.

### Lessons Learned

#### Design & Operations Mindset

- **Proactive instead of Reactive:** Always prepare for the worst-case scenario (Disaster Recovery).
- **Automation-first:** Any task repeated more than twice must be automated.
- **Immutable Infrastructure:** The immutable infrastructure mindset – instead of modifying the server directly (SSH-ing to fix configs), update the IaC code and deploy a new server.

#### Technical Architecture

- **CI/CD Pipelines:** Understanding the clear steps to build a standard pipeline from Source Code → Build → Test → Deploy.
- The importance of clearly **separating environments** (Dev, Staging, Production) to isolate risks.
- Understanding how configuration and infrastructure management tools work to ensure consistency across environments.

#### Implementation Strategy

- **Start small:** No need to adopt DevOps comprehensively all at once. Start by automating testing, then building, and finally deployment.
- Build a **Post-mortem culture**: When a disaster occurs, focus on finding the Root Cause instead of pointing fingers (Blameless culture).

### Application to Career Orientation

- **Building CI/CD:** Apply automated pipeline setups for personal Fullstack projects to prepare for becoming a true Fullstack Engineer, fully understanding the product lifecycle from code to deployment.
- **Applying IaC on AWS:** Instead of manually creating VPCs, EC2s, or configuring networks on the AWS Console, transition to writing automation scripts using CloudFormation or Terraform.
- **Optimizing monitoring systems:** Integrate systems like Nagios or AWS CloudWatch for Linux servers (especially CentOS) to track network metrics and receive early warnings before disasters strike.
- **Professional systems administration:** Limit the habit of directly SSH-ing into servers for hotfixes; instead, manage configurations centrally via Git.

### Experience at the Event

Attending the event **“THE HIDDEN ICEBERG OF A PROJECT: DEVOPS BEFORE DISASTER”** was a practical and eye-opening experience, helping me rethink how tech projects are operated. Some standout experiences included:

#### Lessons from Real "Disasters"
- The speakers dissected real-world case studies of projects crashing due to ignoring the "submerged part of the iceberg." This helped me realize the unpredictable consequences of manual work and lacking a system testing process.

#### Practical Technical Approach
- Got introduced to the real-world workflow of CI/CD pipelines and how DevOps engineers automate infrastructure. 
- Gained a deeper understanding of the importance of building proactive monitoring systems (observability) to "see through" the hidden parts of a project, rather than just configuring a server to run and leaving it at that.

#### Team Culture Mindset
- Realized that the biggest barrier in tech projects is not technology, but the lack of communication between the Dev and Ops teams. The workshop emphasized the culture of shared responsibility, a crucial mindset for future system/Fullstack engineering orientations.

#### Key Takeaways
- Adopting a DevOps culture early will help control risks, minimize downtime, and avoid nasty surprises later on. 
- Automating and monitoring network/server systems right from the start is the most profitable investment in terms of time and stability for any project.

#### Some event photos
  (/images/event.jpg)
  (/images/enven2.jpg)



