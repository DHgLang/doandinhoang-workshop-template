---
title: "Week 9 Worklog"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
### Week 9 goals:
* Build the serverless backend: API Gateway, Lambda, DynamoDB, SQS.
* Complete seat-lock and async booking creation flow.

### Tasks:
| Day | Work | Start | End | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Add booking-api Lambda + HTTP API (movie-booking-api).<br>- Routes GET /health, ANY /{proxy+}. | 06/07/2026 | 06/07/2026 | API Gateway HTTP API |
| 3 | - Create DynamoDB BookingStoreTable (pk/sk, TTL).<br>- Map Amplify Data tables (Movie, Booking, Ticket…). | 07/07/2026 | 07/07/2026 | DynamoDB single-table |
| 4 | - Create SQS BookingQueue + DLQ.<br>- booking-worker Lambda consumes the queue. | 08/07/2026 | 08/07/2026 | SQS + Lambda ESM |
| 5 | - Seat-lock / create-booking APIs.<br>- Set VITE_API_URL from amplify_outputs.json. | 09/07/2026 | 09/07/2026 | Project backend.ts |
| 6 | - Test /health, /movies, seat lock on sandbox.<br>- Review least-privilege Lambda IAM roles. | 10/07/2026 | 10/07/2026 | AWS Console |

### Outcomes:
* Serverless backend live: API → Lambda → DynamoDB / SQS.
* Sync booking path + async worker running in sandbox.
