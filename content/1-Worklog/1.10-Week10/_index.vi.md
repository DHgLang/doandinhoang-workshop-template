---
title: "Worklog Tuần 10"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
### Mục tiêu tuần 10:
* Tích hợp thanh toán VNPay sandbox và hoàn thiện e-ticket.
* Bật CloudWatch RUM; xử lý lỗi API / CORS / env khi demo.

### Các công việc cần triển khai:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Cấu hình VNPAY_TMN_CODE, VNPAY_HASH_SECRET.<br>- API tạo URL thanh toán + return URL. | 13/07/2026 | 13/07/2026 | VNPay sandbox docs |
| 3 | - UI Checkout → redirect VNPay → Payment result.<br>- Phát hành e-ticket (mã vé / QR placeholder). | 14/07/2026 | 14/07/2026 | Frontend payment flow |
| 4 | - Bật CloudWatch RUM (spirit-movie-rum).<br>- Gắn RUM SDK trên frontend. | 15/07/2026 | 15/07/2026 | CloudWatch RUM |
| 5 | - Debug CORS, env, seat lock TTL.<br>- Xem Lambda logs / API latency trên CloudWatch. | 16/07/2026 | 16/07/2026 | CloudWatch Logs |
| 6 | - Hoàn thiện Admin: Dashboard, Movies, Bookings, Traffic.<br>- Gán user vào nhóm Cognito admin. | 17/07/2026 | 17/07/2026 | Cognito Groups |

### Kết quả đạt được:
* Thanh toán VNPay sandbox và e-ticket hoạt động end-to-end.
* RUM + Admin Traffic hỗ trợ quan sát hiệu năng thực tế.
