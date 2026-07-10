---
title: "Worklog Tuần 11"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
### Mục tiêu tuần 11:
* Deploy frontend production lên Amplify Hosting.
* Bật WAF bảo vệ edge; kiểm thử E2E trên URL live.

### Các công việc cần triển khai:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - npm run build production.<br>- Script deploy-hosting.ps1 upload zip Amplify. | 20/07/2026 | 20/07/2026 | Amplify Hosting |
| 3 | - Xác nhận URL live main.d2zv6ka00i1nyo.amplifyapp.com.<br>- Đồng bộ FRONTEND_URL / VNPay return URL. | 21/07/2026 | 21/07/2026 | Amplify Console |
| 4 | - Tạo WAF Web ACL (CloudFront / us-east-1).<br>- Bật managed rules; gắn firewall trên Amplify. | 22/07/2026 | 22/07/2026 | AWS WAF |
| 5 | - Test E2E: duyệt phim → ghế → VNPay → vé.<br>- Kiểm tra Admin + /health trên production. | 23/07/2026 | 23/07/2026 | Live app |
| 6 | - Public repo GitHub; cập nhật README / DEPLOY docs.<br>- Ghi lại kiến trúc và checklist vận hành. | 24/07/2026 | 24/07/2026 | GitHub |

### Kết quả đạt được:
* Frontend production ổn định trên Amplify Hosting + WAF.
* Luồng đặt vé E2E chạy được trên môi trường live.
