---
title: "Worklog Tuần 8"
date: 2026-05-05
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu tuần 8:
* Chuyển sang giai đoạn phát triển **Movie Ticket Booking Platform**.
* Khởi tạo dự án Amplify Gen 2 + React (Vite), thiết lập Cognito và khung frontend.

### Các công việc cần triển khai:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Khởi tạo monorepo (thư mục frontend + amplify).<br>- Cài Node.js, AWS CLI, cấu hình region ap-southeast-1. | 29/06/2026 | 29/06/2026 | Amplify Gen 2 docs |
| 3 | - Định nghĩa Auth (Cognito User Pool, nhóm admin).<br>- Tạo schema Amplify Data (Movie, Cinema, Showtime…). | 30/06/2026 | 30/06/2026 | Amplify Auth / Data |
| 4 | - Scaffold React app (Vite): trang chủ, Movies, Login.<br>- Tích hợp Amplify client (file amplify_outputs.json). | 01/07/2026 | 01/07/2026 | React + Amplify UI |
| 5 | - Chạy npm run sandbox lần đầu.<br>- Kiểm tra Cognito đăng ký / đăng nhập. | 02/07/2026 | 02/07/2026 | ampx sandbox |
| 6 | - Hoàn thiện cấu trúc thư mục, file .env.example.<br>- Commit source lên GitHub. | 03/07/2026 | 03/07/2026 | Git / GitHub |

### Kết quả đạt được:
* Dự án Amplify Gen 2 + React chạy được trên sandbox.
* Cognito và khung UI đặt vé sẵn sàng mở rộng backend booking.
