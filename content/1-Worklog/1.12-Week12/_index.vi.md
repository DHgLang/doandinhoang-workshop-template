---
title: "Worklog Tuần 12"
date: 2026-05-11
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Hoàn thiện báo cáo thực tập Hugo (Workshop 5.1–5.6), tài liệu kỹ thuật và slide thuyết trình.
* Tổng kết kiến trúc **Movie Ticket Booking Platform**; chuẩn bị demo live và dọn dẹp sandbox.
* Kiểm tra chi phí trên AWS Billing; hoàn thiện tài liệu song ngữ trước khi kết thúc kỳ thực tập.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Cập nhật Hugo Workshop: tổng quan kiến trúc, Prerequisite, Backend sandbox<br>- Chụp / gắn ảnh Console (Cognito, API Gateway, DynamoDB, SQS, Lambda) | 27/07/2026 | 28/07/2026 | Hugo template + AWS Console |
| 3 | - Hoàn thiện mục Frontend & Hosting, Demo luồng khách hàng / Admin<br>- Gắn ảnh live app, VNPay, RUM, WAF | 29/07/2026 | 30/07/2026 | App live + Amplify Console |
| 4 | - Viết mục Dọn dẹp (sandbox delete) và Tổng quan & chi phí (Billing)<br>- Cập nhật Worklog tuần 8–12, Proposal cho khớp stack DynamoDB / Amplify | 31/07/2026 | 03/08/2026 | AWS Billing + báo cáo Hugo |
| 5 | - Soạn slide thuyết trình tổng kết kiến trúc và demo<br>- Rà soát Event / Self-Assessment / Feedback | 04/08/2026 | 07/08/2026 | Tài liệu cá nhân |
| 6 | - Demo với Mentor; bảo vệ báo cáo<br>- Chạy `npx ampx sandbox delete`; xác nhận CloudFormation / DynamoDB<br>- Kiểm tra AWS Billing; kết thúc kỳ thực tập | 10/08/2026 | 11/08/2026 | Cleanup checklist |

### Kết quả đạt được tuần 12:

* Hoàn thiện báo cáo Hugo song ngữ: Workshop 5.1–5.6 (Prerequisite → Backend → Frontend → Demo → Cleanup → Cost).
* Tổng hợp kiến trúc end-to-end: Amplify Gen 2, Cognito, API Gateway, Lambda, DynamoDB, SQS, VNPay, Amplify Hosting, WAF, CloudWatch RUM.
* Chuẩn bị demo live luồng đặt vé (chọn ghế → thanh toán → e-ticket) và bảng Admin.
* Thực hiện dọn dẹp Amplify sandbox; xác nhận stack sandbox đã xóa, DynamoDB Tables (0), giữ CDKToolkit.
* Đối chiếu chi phí trên AWS Billing (free plan / credits); ghi nhận trong mục Tổng quan & chi phí.
* Hoàn thiện Worklog, Proposal, Events, Self-Assessment và tài liệu thuyết trình cuối kỳ.
