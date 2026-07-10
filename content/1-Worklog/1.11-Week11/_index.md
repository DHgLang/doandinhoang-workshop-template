---
title: "Week 11 Worklog"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
### Week 11 goals:
* Deploy the production frontend to Amplify Hosting.
* Enable edge WAF; run E2E tests on the live URL.

### Tasks:
| Day | Work | Start | End | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Production npm run build.<br>- deploy-hosting.ps1 zip upload to Amplify. | 20/07/2026 | 20/07/2026 | Amplify Hosting |
| 3 | - Confirm live URL main.d2zv6ka00i1nyo.amplifyapp.com.<br>- Sync FRONTEND_URL / VNPay return URL. | 21/07/2026 | 21/07/2026 | Amplify Console |
| 4 | - Create WAF Web ACL (CloudFront / us-east-1).<br>- Enable managed rules; turn on Amplify firewall. | 22/07/2026 | 22/07/2026 | AWS WAF |
| 5 | - E2E test: movies → seats → VNPay → ticket.<br>- Verify Admin + /health on production. | 23/07/2026 | 23/07/2026 | Live app |
| 6 | - Public GitHub repo; update README / DEPLOY docs.<br>- Record architecture and ops checklist. | 24/07/2026 | 24/07/2026 | GitHub |

### Outcomes:
* Production frontend stable on Amplify Hosting + WAF.
* End-to-end booking flow works on the live environment.
