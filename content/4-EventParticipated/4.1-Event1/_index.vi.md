---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
disableToc: true
---


# BÀI THU HOẠCH AWS MEETUP

| Thông tin | Chi tiết |
|------------|----------|
| **Tên sự kiện** | Mini Meetup – First Cloud AI Journey \| 06/06/2026 |
| **Thời gian** | Ngày 06/06/2026 |
| **Địa điểm** | Tầng 26, Tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, Thành phố Hồ Chí Minh |
| **Vai trò** | Người tham dự |

---

## 1. Mục đích của sự kiện

Sự kiện được tổ chức nhằm tạo sân chơi học thuật dành cho học viên chương trình **First Cloud AI Journey (FCJ)**, giúp củng cố kiến thức về điện toán đám mây, các dịch vụ AWS, bảo mật, AI và lộ trình nghề nghiệp thông qua các bài chia sẻ kỹ thuật thực chiến từ chính các bạn trong chương trình.

Bên cạnh đó, chương trình tạo điều kiện để học viên giao lưu, đặt câu hỏi trực tiếp, học hỏi kinh nghiệm triển khai từ đồng đội và mentor. Đây cũng là cơ hội để gắn kiến thức trên Cloud Journey với dự án thực tập cá nhân, thay vì chỉ học lý thuyết trên tài liệu.

Không khí offline khuyến khích tinh thần tự học, phản biện kỹ thuật và chia sẻ công khai những gì đã làm được trong thời gian thực tập — góp phần xây dựng cộng đồng học tập gắn kết hơn trong FCJ.

---

## 2. Ban tổ chức và thành phần tham gia

Chương trình có sự tham gia của:

- Ban tổ chức chương trình **The First Cloud Journey – AWS Việt Nam**, phụ trách lịch trình, địa điểm và điều phối buổi chia sẻ.
- Các Mentor và Trainer của chương trình AWS / FCJ, hỗ trợ định hướng nội dung và góp ý kỹ thuật khi cần.
- Các diễn giả là học viên đã chuẩn bị slide, demo và trình bày chủ đề mình nghiên cứu trong quá trình thực tập.
- Người tham dự là học viên trong chương trình, lắng nghe, ghi chép và trao đổi sau mỗi bài.

Sự kết hợp giữa ban tổ chức, mentor và học viên giúp buổi meetup vừa mang tính học thuật, vừa gần với trải nghiệm thực tế của người đang học Cloud.

---

## 3. Nội dung nổi bật

Điểm nhấn của chương trình là chuỗi bài chia sẻ kỹ thuật offline. Các chủ đề chính gồm:

- **Docker (Bảo Huỳnh)** — so sánh virtualization và containerization; giải thích image, container, layer cache; nêu lợi ích portability và use case CI/CD, microservices, modernize legacy. Em hiểu rõ hơn vì sao container phù hợp môi trường cloud-native.
- **AWS WAF + Machine Learning (Lê Hoàng Gia Đại)** — Web ACL, Managed Rules, rate limiting; hạn chế của rule-based trước zero-day; pipeline ML (dataset CSE-CIC-IDS2018, LightGBM) kết hợp log WAF và cảnh báo. Kiến trúc đề cập VPC, ALB, S3, Lambda, GuardDuty, CloudWatch, SNS.
- **Multiplayer Godot với AWS WebSocket (Nguyễn Quốc Bảo)** — chọn WebSocket cho turn-based/lobby; Lambda xử lý CONNECT / DISCONNECT / MESSAGE; lưu state trên DynamoDB; bài học về stale connection và chi phí Scan. Hướng mở rộng GameLift cho game realtime cao tần.
- **GraphRAG với Amazon Bedrock & Neptune (Việt Phát)** — giới hạn RAG text thuần với câu hỏi multi-hop; GraphRAG lưu quan hệ qua edges; Bedrock Knowledge Bases + Neptune Analytics hoặc pipeline LlamaIndex tùy chỉnh.
- **Lộ trình Helpdesk → Sysadmin → Cloud/DevOps (Trần Trung Vinh)** — kỹ năng nền từ support, tự học Linux/networking, automate và monitor; chuyển mindset on-prem sang AWS, IaC, CI/CD; nhấn mạnh portfolio thực tế hơn chứng chỉ đơn thuần.

Không khí buổi chia sẻ sôi nổi: có demo trực tiếp, hỏi đáp sau mỗi bài, trao đổi trade-off thực tế về cost, latency và bảo mật. Em thấy rõ mức độ chuẩn bị của từng diễn giả và cách họ trình bày bài toán end-to-end.

---

## 4. Những gì học được

Thông qua sự kiện, em đã học và củng cố được nhiều kiến thức quan trọng:

- Ôn tập và mở rộng kiến thức AWS / Cloud đã học trong chương trình FCJ, đặc biệt các dịch vụ gắn với bảo mật, serverless và AI.
- Hiểu rõ hơn cách áp dụng Docker, WAF, API Gateway WebSocket, Lambda, DynamoDB và GraphRAG vào bài toán thực tế thay vì chỉ nhớ tên dịch vụ.
- Tiếp cận Best Practices về bảo mật edge, quản lý state serverless (stateless Lambda + DB), và observability bằng CloudWatch / cảnh báo.
- Rèn luyện khả năng lắng nghe kỹ thuật, ghi chép có cấu trúc và liên hệ ngay với dự án **Movie Ticket Booking Platform**.
- Nâng cao nhận thức về lộ trình nghề Cloud/DevOps: nền tảng vận hành hệ thống, tự học liên tục và thực hành lab là then chốt.

Những nội dung này giúp em nhìn lại khoảng trống kiến thức của bản thân và ưu tiên học sâu hơn các phần còn yếu sau meetup.

---

## 5. Ứng dụng vào công việc

Những kiến thức thu nhận được có thể áp dụng trực tiếp vào dự án thực tập và định hướng công việc sau này:

- **Docker:** container hóa môi trường dev của movie-booking để đồng đội chạy đồng nhất; hướng tới CI/CD build trước khi deploy Amplify Hosting.
- **WAF + giám sát:** củng cố lý do gắn **AWS WAF** trên CloudFront cho frontend production; theo dõi metrics / RUM trong Admin thay vì chỉ kiểm tra “site mở được”.
- **Serverless realtime / queue:** kiến trúc WebSocket + Lambda + DynamoDB rất gần stack đặt vé (API Gateway, Lambda, DynamoDB, SQS) — giúp xử lý booking bất đồng bộ và worker đúng cách hơn.
- **GraphRAG / AI:** định hướng mở rộng sau khi hoàn thiện core booking (gợi ý phim, chatbot hỗ trợ) bằng Bedrock + knowledge graph thay vì RAG text thuần.
- **Tư duy vận hành (Vinh Trần):** automate, monitor, document — áp dụng khi giữ/xóa sandbox, kiểm tra Billing, tránh thao tác nóng thiếu kiểm soát trên AWS.

Nhìn chung, meetup giúp em chuyển từ “làm cho chạy” sang “làm cho an toàn, quan sát được và dễ vận hành”.

---

## 6. Trải nghiệm trong sự kiện

### Học hỏi từ diễn giả và mentor

Các bài trình bày xuất phát từ mini-project thật (có kiến trúc, demo, thách thức và hướng cải tiến). Em học được cách trình bày trade-off thay vì chỉ liệt kê dịch vụ AWS. Mentor và không khí hỏi đáp giúp làm rõ những điểm còn mơ hồ ngay tại chỗ.

### Trải nghiệm kỹ thuật thực tế

Buổi offline khác hẳn xem slide một mình: có thể hỏi ngay sau demo — ví dụ vì sao DynamoDB Scan tốn cost trong matchmaking, khi nào chọn WebSocket thay REST, hoặc WAF rule-based thiếu gì so với ML NIDS. Việc thấy demo live (Dockerfile, dashboard, game Godot) giúp kiến thức “dính” hơn lý thuyết.

### Tiếp cận các dịch vụ / công nghệ AWS

Thông qua chương trình, em làm quen sâu hơn với Docker/container, AWS WAF, CloudWatch, API Gateway WebSocket, Lambda, DynamoDB, Amazon Bedrock, Amazon Neptune (GraphRAG), cùng tư duy Cloud/DevOps và lộ trình nghề. Em hiểu rõ hơn cách các thành phần kết hợp thành một hệ thống hoàn chỉnh.

### Giao lưu và kết nối

Em có cơ hội giao lưu với học viên FCJ và diễn giả, trao đổi ý tưởng gắn với dự án thực tập, và học thói quen chuẩn bị slide/demo trước khi trình bày. Đây là kỹ năng hữu ích cho báo cáo thực tập và phỏng vấn kỹ thuật sau này.

---

## 7. Bài học rút ra

Sau khi tham gia sự kiện, em rút ra một số bài học quan trọng:

- Cần nắm vững kiến thức nền và thực hành thường xuyên trên AWS; chỉ học lý thuyết sẽ khó phản xạ khi gặp tình huống thật.
- Các chủ đề Docker, WAF, serverless và AI bổ sung cho nhau khi xây hệ thống end-to-end — thiếu một lớp (ví dụ bảo mật hoặc giám sát) sẽ làm giải pháp yếu đi.
- Học từ peer và hỏi đáp trực tiếp giúp phát hiện lỗ hổng kiến thức nhanh hơn tự học đơn lẻ.
- Dự án thực tập cần đi kèm bảo mật, giám sát và quy trình triển khai — không chỉ dừng ở “feature chạy được”.
- Chuẩn bị và trình bày kỹ thuật cũng là một phần năng lực nghề nghiệp, không kém phần code.

---

## 8. Kết luận

Mini Meetup ngày **06/06/2026** tại Bitexco là hoạt động học thuật ý nghĩa, giúp học viên vừa ôn tập kiến thức AWS/FCJ, vừa học hỏi kinh nghiệm thực chiến từ các bài chia sẻ của đồng đội. Em củng cố chuyên môn, gắn được nội dung sự kiện với dự án **Movie Ticket Booking Platform**, và có thêm động lực tiếp tục theo đuổi Cloud Computing cũng như định hướng AI trên AWS trong các giai đoạn học tập tiếp theo.
