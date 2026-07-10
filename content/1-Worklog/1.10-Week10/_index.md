---
title: "Week 10 Worklog"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
### Week 10 goals:
* Integrate VNPay sandbox payment and finish e-ticket issuance.
* Enable CloudWatch RUM; fix API / CORS / env issues during demos.

### Tasks:
| Day | Work | Start | End | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Configure VNPAY_TMN_CODE, VNPAY_HASH_SECRET.<br>- Payment URL API + return URL. | 13/07/2026 | 13/07/2026 | VNPay sandbox docs |
| 3 | - Checkout UI → VNPay redirect → payment result.<br>- Issue e-ticket (ticket code / QR placeholder). | 14/07/2026 | 14/07/2026 | Frontend payment flow |
| 4 | - Enable CloudWatch RUM (spirit-movie-rum).<br>- Attach RUM SDK on the frontend. | 15/07/2026 | 15/07/2026 | CloudWatch RUM |
| 5 | - Debug CORS, env, seat-lock TTL.<br>- Review Lambda logs / API latency in CloudWatch. | 16/07/2026 | 16/07/2026 | CloudWatch Logs |
| 6 | - Finish Admin: Dashboard, Movies, Bookings, Traffic.<br>- Add user to Cognito admin group. | 17/07/2026 | 17/07/2026 | Cognito Groups |

### Outcomes:
* VNPay sandbox payment and e-ticket work end-to-end.
* RUM + Admin Traffic provide real-user performance visibility.
