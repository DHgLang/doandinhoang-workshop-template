---
title: "Worklog Tuần 9"
date: 2026-05-05
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:
* Xây dựng backend serverless: API Gateway, Lambda, DynamoDB, SQS.
* Hoàn thiện luồng khóa ghế và tạo booking bất đồng bộ.

### Các công việc cần triển khai:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Thêm Lambda booking-api + HTTP API (movie-booking-api).<br>- Route GET /health, ANY /{proxy+}. | 06/07/2026 | 06/07/2026 | API Gateway HTTP API |
| 3 | - Tạo DynamoDB BookingStoreTable (pk/sk, TTL).<br>- Map Amplify Data tables (Movie, Booking, Ticket…). | 07/07/2026 | 07/07/2026 | DynamoDB single-table |
| 4 | - Tạo SQS BookingQueue + DLQ.<br>- Lambda booking-worker consume queue. | 08/07/2026 | 08/07/2026 | SQS + Lambda ESM |
| 5 | - API lock seats / create booking.<br>- Cập nhật VITE_API_URL từ amplify_outputs.json. | 09/07/2026 | 09/07/2026 | Project backend.ts |
| 6 | - Kiểm thử /health, /movies, lock ghế trên sandbox.<br>- Review IAM role tối thiểu cho Lambda. | 10/07/2026 | 10/07/2026 | AWS Console |

### Kết quả đạt được:
* Backend serverless hoạt động: API → Lambda → DynamoDB / SQS.
* Luồng đặt vé đồng bộ + worker bất đồng bộ chạy trên sandbox.
