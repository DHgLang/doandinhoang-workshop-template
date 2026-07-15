---
title: "Week 3 Worklog"
date: 2026-05-05
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
### Week 3 Objectives:
* Deploy shared storage systems (NFS) on the Cloud using Amazon EFS.
* Verify system performance with practical measurement tools.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Explore EFS architecture:<br>&emsp; + Mount targets & Security Groups.<br>&emsp; + Performance Modes (General, Max I/O). | 25/05/2026 | 25/05/2026 | Amazon EFS documentation |
| Tue | - **EFS Practice:**<br>&emsp; + Create Amazon EFS File System.<br>&emsp; + Configure Mount Targets for VPC Subnets. | 26/05/2026 | 26/05/2026 | EFS mount targets & VPC guides |
| Wed | - **NFS Connection:**<br>&emsp; + Mount EFS to multiple EC2 instances.<br>&emsp; + Configure `/etc/fstab` for auto-mount at boot. | 27/05/2026 | 27/05/2026 | EFS mounting on EC2 / fstab guides |
| Thu | - Stress-test tools:<br>&emsp; + Explore `dd` command for I/O testing.<br>&emsp; + Benchmark actual read/write on EFS. | 28/05/2026 | 28/05/2026 | Linux dd I/O benchmarking references |
| Fri | - **Performance Report:**<br>&emsp; + Test 1GiB read/write.<br>&emsp; + Log results and optimize settings. | 29/05/2026 | 29/05/2026 | EFS performance modes documentation |

### Results achieved in Week 3:
* Successfully set up shared EFS storage across multiple EC2 instances.
* Learned how to configure auto-mounting of NFS on Linux.
* Mastered performance benchmarking techniques using the `dd` tool.
