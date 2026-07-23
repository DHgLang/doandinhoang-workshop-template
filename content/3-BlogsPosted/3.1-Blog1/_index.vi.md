---
title: "Blog 1"
date: 2026-07-21
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Vì sao Amazon Bedrock AgentCore chọn Cedar để kiểm soát quyền của AI Agent?

Các AI Agent ngày càng có khả năng thực hiện nhiều tác vụ thay con người như đọc tài liệu, gọi API, truy cập cơ sở dữ liệu hay thao tác với nhiều dịch vụ khác nhau. Điều này cũng đặt ra một câu hỏi quan trọng:

**Làm thế nào để đảm bảo AI Agent chỉ thực hiện những hành động mà nó được phép làm?**

AWS đã chia sẻ khá chi tiết về quyết định sử dụng Cedar làm ngôn ngữ chính sách (policy language) trong Amazon Bedrock AgentCore, thay vì chỉ dựa vào prompt hoặc các quy tắc kiểm tra đơn giản.

## 1. Bài toán đặt ra

Trong nhiều ứng dụng AI hiện nay, quyền truy cập thường được kiểm tra ngay từ đầu phiên làm việc. Ví dụ:

- Người dùng đăng nhập thành công.
- Agent nhận yêu cầu.
- Agent lần lượt gọi nhiều công cụ (tool calling).

Tuy nhiên, quyền của Agent không chỉ nên được kiểm tra một lần.

Giả sử Agent cần:

- đọc tài liệu nội bộ,
- truy vấn cơ sở dữ liệu,
- gửi email,
- tạo ticket,
- gọi API của hệ thống khác.

Mỗi hành động đều có mức độ nhạy cảm khác nhau và có thể cần những điều kiện riêng. Nếu chỉ kiểm tra quyền ở đầu phiên, Agent có thể thực hiện những thao tác vượt quá phạm vi được phép.

## 2. Cedar là gì?

Cedar là ngôn ngữ định nghĩa chính sách (policy language) do AWS phát triển nhằm xây dựng các hệ thống phân quyền theo nguyên tắc fine-grained authorization.

Thay vì hard-code quyền trong ứng dụng, Cedar mô tả rõ:

- **Principal** — ai thực hiện?
- **Action** — được phép làm gì?
- **Resource** — trên tài nguyên nào?
- **Context** — trong điều kiện nào?

Trong ngữ cảnh **AgentCore Gateway**, có thể hiểu gần như sau: Principal thường là identity của User hoặc Agent session (thường qua OAuth/IAM token) khi gọi tool; Action là lệnh gọi tool (MCP tool invocation); Resource là tool/API hoặc dữ liệu cần tương tác; Context bổ sung điều kiện như tham số đầu vào hay ngữ cảnh phiên.

Mỗi yêu cầu đều được đánh giá dựa trên các thành phần này trước khi cho phép thực hiện.

## 3. Vì sao Agent cần Policy Engine?

Điểm mình thấy thú vị nhất trong bài viết là AWS tách biệt hoàn toàn khả năng và quyền hạn của Agent.

Một Agent có thể biết cách:

- gọi API,
- đọc tài liệu,
- chạy workflow,
- sử dụng nhiều công cụ khác nhau.

Nhưng điều đó không đồng nghĩa Agent luôn được phép thực hiện mọi hành động.

Policy Engine đóng vai trò như một lớp kiểm soát độc lập: gắn với Gateway, đánh giá từng yêu cầu trước khi Agent truy cập tài nguyên. Đặc biệt, AgentCore Gateway áp dụng cơ chế **Default Deny** — mặc định chặn tất cả các cuộc gọi tool. Agent chỉ được thực hiện những gì được cấp quyền rõ ràng trong Cedar policy (ví dụ `permit(...)`).

Không chỉ chặn lúc gọi API ở runtime, Cedar còn hỗ trợ **Tool Filtering** (partial evaluation): ẩn các tool mà Agent chắc chắn không có quyền khỏi danh sách tool khả dụng (ví dụ kết quả `list_tools`). Agent không thấy tool thì giảm mạnh nguy cơ cố tình hoặc vô tình gọi nhầm.

Điều này giúp giảm nguy cơ:

- Prompt injection khiến Agent thực hiện hành động ngoài ý muốn.
- Agent vô tình truy cập dữ liệu nhạy cảm.
- Công cụ (tool) bị lạm dụng vượt quá phạm vi được cấp quyền.

## 4. Kết luận

Theo mình, điểm đáng học nhất không phải Cedar là một ngôn ngữ policy mới, mà là cách AWS tách authorization khỏi logic của Agent.

Điều này khá giống các ứng dụng web hiện đại: chúng ta không hard-code quyền truy cập trong từng API mà sử dụng một lớp phân quyền tập trung.

Khi áp dụng cho AI Agent, cách tiếp cận này giúp việc mở rộng và quản lý quyền trở nên rõ ràng hơn, đặc biệt khi Agent ngày càng có khả năng sử dụng nhiều công cụ và thực hiện các workflow phức tạp.

Tuy nhiên, Policy Engine cũng không phải “lá chắn” duy nhất. Một hệ thống AI Agent an toàn vẫn cần kết hợp thêm:

- IAM và nguyên tắc least privilege,
- sandbox cho các tác vụ thực thi mã,
- Guardrails để kiểm soát nội dung,
- logging và theo dõi toàn bộ quá trình Agent hoạt động,
- human-in-the-loop với các hành động có rủi ro cao.

Policy quyết định Agent được phép làm gì, còn Guardrails giúp Agent nên phản hồi như thế nào. Hai lớp này bổ sung cho nhau chứ không thể thay thế nhau.

---

## 5. Kiến trúc

<img src="/images/3-BlogsPosted/3.1-Blog1/ArchitectureBlog1.png" alt="Architecture Diagram" style="max-width:70%;height:auto;" />

## 6. Nguồn tham khảo

- [Why Policy in Amazon Bedrock AgentCore chose Cedar for securing agentic workflows](https://aws.amazon.com/blogs/security/why-policy-in-amazon-bedrock-agentcore-chose-cedar-for-securing-agentic-workflows/)
- [Amazon Bedrock AgentCore Policy](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/policy.html)

<img src="/images/3-BlogsPosted/3.1-Blog1/Blog1.png" alt="Blog1 Facebook post" style="max-width:42%;height:auto;" />
