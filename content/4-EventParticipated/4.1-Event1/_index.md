---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
disableToc: true
---


# AWS MEETUP EVENT REPORT

| Information | Details |
|-------------|---------|
| **Event Name** | Mini Meetup – First Cloud AI Journey \| 06/06/2026 |
| **Date & Time** | June 6, 2026 |
| **Venue** | 26th Floor, Bitexco Financial Tower, 02 Hai Trieu Street, Sai Gon Ward, Ho Chi Minh City, Vietnam |
| **Role** | Attendee |

---

## 1. Purpose of the Event

The event was organized as an academic knowledge-sharing activity for **First Cloud AI Journey (FCJ)** students. Its purpose was to strengthen understanding of Cloud Computing, AWS services, security, AI, and career paths through practical technical talks delivered by peers in the program.

It also created space for live Q&A, peer exchange, and connecting Cloud Journey coursework with each student’s internship project — instead of learning only from documentation.

The offline format encouraged self-learning, technical discussion, and openly sharing what interns had built during the program, helping strengthen the FCJ learning community.

---

## 2. Speakers and Organizers

The event involved:

- The organizing team of **The First Cloud Journey – AWS Vietnam**, responsible for schedule, venue, and session coordination.
- Mentors and trainers from the AWS / FCJ program, supporting content direction and technical feedback when needed.
- Student speakers who prepared slides, demos, and presented topics researched during the internship.
- Attendees from the cohort who listened, took notes, and joined discussions after each talk.

This mix of organizers, mentors, and students kept the meetup both academic and grounded in real learning experiences.

---

## 3. Event Highlights

The highlight was an offline technical sharing series. Main topics included:

- **Docker (Bao Huynh)** — virtualization vs containerization; images, containers, layer caching; portability benefits and CI/CD / microservices / legacy modernization use cases. This clarified why containers fit cloud-native work.
- **AWS WAF + Machine Learning (Le Hoang Gia Dai)** — Web ACL, Managed Rules, rate limiting; limits of rule-based defenses against zero-days; ML pipeline (CSE-CIC-IDS2018, LightGBM) correlated with WAF logs and alerts. Architecture touched VPC, ALB, S3, Lambda, GuardDuty, CloudWatch, SNS.
- **Godot multiplayer with AWS WebSocket (Nguyen Quoc Bao)** — WebSocket for turn-based/lobby flows; Lambda CONNECT / DISCONNECT / MESSAGE handlers; DynamoDB for state; lessons on stale connections and Scan cost; GameLift as a path for high-frequency realtime games.
- **GraphRAG with Amazon Bedrock & Neptune (Viet Phat)** — limits of plain-text RAG on multi-hop questions; relationship edges in a graph; Bedrock Knowledge Bases + Neptune Analytics or a custom LlamaIndex pipeline.
- **Career path Helpdesk → Sysadmin → Cloud/DevOps (Tran Trung Vinh)** — support fundamentals, self-learning Linux/networking, automate and monitor; shift from on-prem to AWS, IaC, CI/CD; real portfolio valued over certificates alone.

The atmosphere was energetic, with live demos and practical trade-off discussions on cost, latency, and security. Preparation quality and end-to-end storytelling from each speaker stood out.

---

## 4. Knowledge Gained

Through the event, I reviewed and strengthened:

- AWS / Cloud knowledge from the FCJ program, especially security, serverless, and AI-related services.
- How Docker, WAF, API Gateway WebSocket, Lambda, DynamoDB, and GraphRAG apply to real problems — not only service names.
- Best practices for edge security, serverless state (stateless Lambda + database), and CloudWatch-based observability.
- Structured note-taking and immediate mapping of talks to **Movie Ticket Booking Platform**.
- Awareness of Cloud/DevOps career progression: operations fundamentals, continuous self-learning, and hands-on labs.

These takeaways helped me identify personal knowledge gaps and prioritize deeper study after the meetup.

---

## 5. Practical Applications

Knowledge from the meetup applies directly to the internship project and future work:

- **Docker:** containerize movie-booking dev environments for consistent teammate setups; move toward CI/CD builds before Amplify Hosting deploy.
- **WAF + monitoring:** reinforces attaching **AWS WAF** to CloudFront for production frontend; watch metrics / RUM in Admin instead of only checking that the site opens.
- **Serverless realtime / queues:** WebSocket + Lambda + DynamoDB closely mirrors the booking stack (API Gateway, Lambda, DynamoDB, SQS) — improving async booking and worker design.
- **GraphRAG / AI:** a future path after core booking (recommendations, support chatbot) using Bedrock + knowledge graphs instead of plain-text RAG.
- **Operations mindset (Vinh Tran):** automate, monitor, document — useful when keeping/deleting sandboxes, checking Billing, and avoiding uncontrolled hotfixes on AWS.

Overall, the meetup shifted my focus from “make it run” to “make it secure, observable, and operable.”

---

## 6. Event Experience

### Learning from speakers and mentors

Talks came from real mini-projects with architecture, demos, challenges, and next steps. I learned how to present trade-offs instead of only listing AWS services. Mentors and Q&A clarified unclear points on the spot.

### Practical technical experience

Offline sessions differ from reading slides alone: I could ask immediately after demos — for example why DynamoDB Scan is costly in matchmaking, when to choose WebSocket over REST, or what rule-based WAF misses compared with ML NIDS. Live demos (Dockerfile, dashboards, Godot on AWS) made concepts stick better than theory.

### Exposure to AWS services and technologies

The session deepened familiarity with Docker/containers, AWS WAF, CloudWatch, API Gateway WebSocket, Lambda, DynamoDB, Amazon Bedrock, Amazon Neptune (GraphRAG), plus Cloud/DevOps mindset and career path thinking. It also showed how these pieces combine into a complete system.

### Networking and knowledge exchange

I connected with FCJ peers and speakers, discussed ideas tied to internship projects, and observed how others prepare slides and demos before presenting — useful skills for internship reports and technical interviews.

---

## 7. Lessons Learned

After the event, key lessons were:

- Fundamentals plus regular hands-on AWS practice matter more than theory alone; theory without practice is hard to apply under real constraints.
- Docker, WAF, serverless, and AI topics complement each other in an end-to-end system — missing a layer (security or monitoring) weakens the solution.
- Peer learning and live Q&A reveal knowledge gaps faster than studying alone.
- Internship projects need security, monitoring, and deployment process — not only working features.
- Technical presentation skill is part of professional capability, not secondary to coding.

---

## 8. Conclusion

The Mini Meetup on **June 6, 2026** at Bitexco was a meaningful academic activity that helped review FCJ/AWS knowledge and learn from practical peer talks. I strengthened technical skills, connected the session to **Movie Ticket Booking Platform**, and gained motivation to continue in Cloud Computing and AI on AWS in the next learning stages.
