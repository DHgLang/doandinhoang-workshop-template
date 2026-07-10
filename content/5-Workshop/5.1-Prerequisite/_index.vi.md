---
title: "Chuẩn bị môi trường"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Yêu cầu

| Hạng mục | Phiên bản / ghi chú |
| --- | --- |
| **Node.js** | 18 trở lên |
| **npm** | Đi kèm Node |
| **AWS CLI** | Đã cấu hình profile (`aws configure` hoặc `npx ampx configure profile`) |
| **Region** | `ap-southeast-1` (Singapore) |
| **Git** | Clone repo public |

#### Clone mã nguồn

```powershell
git clone https://github.com/DHgLang/Movie-Ticket-Booking-Platform.git
cd Movie-Ticket-Booking-Platform
npm install
```

Sau khi clone và cài dependency, project có các thư mục chính: `amplify/` (backend), `frontend/` (React), `scripts/` (deploy).

![Cấu trúc project](/images/5-Workshop/5.1-Prerequisite/project-structure.png)

#### Kiểm tra môi trường

```powershell
node -v
aws sts get-caller-identity
```

Chạy `node -v` để xác nhận Node.js ≥ 18 — ví dụ kết quả `v20.15.0` như ảnh dưới.

![Node.js version](/images/5-Workshop/5.1-Prerequisite/node-version.png)

Lệnh `aws sts get-caller-identity` trả về Account ID, ARN và UserId — chứng tỏ AWS CLI đã đăng nhập đúng profile.

![AWS CLI identity](/images/5-Workshop/5.1-Prerequisite/aws-cli.png)

Kiểm tra region mặc định trong `~/.aws/config` phải là `ap-southeast-1` (Singapore) để khớp với sandbox.

![AWS region ap-southeast-1](/images/5-Workshop/5.1-Prerequisite/aws-region.png)

#### Cấu hình biến môi trường

Sau `npm install`, copy file mẫu:

```powershell
# Tự tạo từ .env.example nếu chưa có
copy .env.example .env
notepad .env
```

| Biến | Mục đích |
| --- | --- |
| `VITE_API_URL` | URL API Gateway (sau `npm run sandbox`) |
| `VITE_TMDB_API_KEY` | API key lấy poster phim từ TMDB |
| `TMDB_API_KEY` | Cùng key — dùng phía Lambda |
| `VNPAY_TMN_CODE`, `VNPAY_HASH_SECRET` | VNPay sandbox (khi test thanh toán) |
| `FRONTEND_URL`, `VNPAY_RETURN_URL` | URL callback sau thanh toán |

File `.env` chứa URL API, key TMDB và thông tin VNPay — nhớ che giá trị nhạy cảm trước khi chụp màn hình.

![File .env (che secret)](/images/5-Workshop/5.1-Prerequisite/env-file.png)

{{% notice info %}}
**Lưu ý:** Không commit `.env` và `amplify_outputs.json` lên GitHub — các file này nằm trong `.gitignore`.
{{% /notice %}}

#### Quyền IAM tối thiểu (gợi ý)

Tài khoản AWS cần quyền triển khai Amplify sandbox: CloudFormation, Lambda, API Gateway, DynamoDB, SQS, Cognito, S3, IAM (pass role), CloudWatch. Sinh viên FCJ thường dùng tài khoản lab đã được cấp sẵn policy.

**Bước tiếp theo**

Sau khi chuẩn bị xong → [5.2 Triển khai Backend](../5.2-Backend/)
