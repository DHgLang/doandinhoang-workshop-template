---
title: "Worklog Tuần 3"
date: 2026-05-05
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
### Mục tiêu tuần 3:
* Triển khai hệ thống lưu trữ chia sẻ (NFS) trên Cloud với Amazon EFS.
* Kiểm tra hiệu năng hệ thống bằng các công cụ đo đạc thực tế.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Tìm hiểu kiến trúc EFS:<br>&emsp; + Mount targets & Security Groups.<br>&emsp; + Performance Modes (General, Max I/O). | 25/05/2026 | 25/05/2026 | Tài liệu Amazon EFS |
| 3 | - **Thực hành EFS:**<br>&emsp; + Tạo Amazon EFS File System.<br>&emsp; + Cấu hình Mount Targets cho các VPC Subnets. | 26/05/2026 | 26/05/2026 | Hướng dẫn Mount Targets & VPC cho EFS |
| 4 | - **Kết nối NFS:**<br>&emsp; + Mount EFS vào nhiều EC2 instance.<br>&emsp; + Cấu hình `/etc/fstab` để tự động mount khi boot. | 27/05/2026 | 27/05/2026 | Hướng dẫn mount EFS trên EC2 / fstab |
| 5 | - Công cụ Stress-test:<br>&emsp; + Tìm hiểu lệnh `dd` để tạo file kiểm tra I/O.<br>&emsp; + Đánh giá thông số đọc/ghi thực tế trên EFS. | 28/05/2026 | 28/05/2026 | Tài liệu benchmark I/O với lệnh dd |
| 6 | - **Báo cáo hiệu năng:**<br>&emsp; + Thực hiện test đọc/ghi 1GiB dữ liệu.<br>&emsp; + Lưu log kết quả và tối ưu hóa thiết lập. | 29/05/2026 | 29/05/2026 | Tài liệu Performance Modes của EFS |

### Kết quả đạt được tuần 3:
* Thiết lập thành công hệ thống lưu trữ chia sẻ EFS giữa nhiều máy chủ EC2.
* Hiểu cách cấu hình NFS mount tự động trên Linux.
* Nắm vững kỹ thuật kiểm tra hiệu năng (benchmark) lưu trữ bằng công cụ `dd`.

