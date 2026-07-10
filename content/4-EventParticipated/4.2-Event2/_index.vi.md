---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---



# Bài thu hoạch “THE HIDDEN ICEBERG OF A PROJECT: DEVOPS BEFORE DISASTER”

### Mục Đích Của Sự Kiện

- Nhận diện những rủi ro ngầm (phần chìm của tảng băng) trong vòng đời phát triển phần mềm.
- Giới thiệu các phương pháp và văn hóa DevOps thực chiến để phòng ngừa thảm họa dự án.
- Hướng dẫn xây dựng tư duy tự động hóa (CI/CD, IaC) và giám sát hệ thống chủ động.
- Gắn kết khoảng cách giữa đội ngũ Development (Phát triển) và Operations (Vận hành).

### Danh Sách Diễn Giả

- **[Tên Diễn Giả ]** -Trần Minh Quân  


### Nội Dung Nổi Bật

#### Thuyết "Tảng Băng Trôi" (The Iceberg Metaphor) trong dự án

- **Bề nổi (Phần nhìn thấy):** Giao diện (UI), tính năng mới, tốc độ release.
- **Phần chìm (Rủi ro tiềm ẩn):** Nợ kỹ thuật (Technical debt), lỗ hổng bảo mật, quy trình deploy thủ công, thiếu cơ chế giám sát, thiếu tài liệu hệ thống.
- **Hậu quả:** Sập hệ thống lúc cao điểm, mất dữ liệu, tốn thời gian fix bug (chữa cháy) thay vì phát triển tính năng mới.

#### Chuyển đổi tư duy: Từ "Chữa cháy" sang "Phòng ngừa" với DevOps

Giải quyết bài toán phần chìm bằng các trụ cột cốt lõi của DevOps:
- **Continuous Integration (CI):** Tích hợp liên tục, phát hiện lỗi sớm (shift-left testing) ngay từ khâu viết code.
- **Continuous Deployment/Delivery (CD):** Tự động hóa luồng đưa sản phẩm lên môi trường thực tế, đảm bảo an toàn và khả năng rollback nhanh chóng.
- **Infrastructure as Code (IaC):** Quản lý và cấp phát hạ tầng bằng code, loại bỏ sai sót do con người thao tác thủ công.

#### Quản lý rủi ro và Giám sát chủ động (Observability)

- **Sự khác biệt giữa Monitoring và Observability:** Không chỉ xem hệ thống sống hay chết, mà phải hiểu *tại sao* nó gặp vấn đề.
- **3 Trụ cột của Observability:** Logs, Metrics, và Traces.
- **Thiết lập cảnh báo (Alerting):** Phát hiện sự cố và gửi thông báo trước khi người dùng kịp nhận ra và phàn nàn.

#### Phá vỡ bức tường Silo (Culture & Collaboration)

- DevOps không phải là một chức danh hay một tool, mà là **văn hóa**.
- Trách nhiệm chia sẻ (Shared Responsibility): Dev cũng cần quan tâm đến cách code chạy trên server, và Ops cũng cần hiểu luồng hoạt động của code.

### Những Gì Học Được

#### Tư Duy Thiết Kế & Vận Hành

- **Proactive thay vì Reactive:** Luôn chuẩn bị cho tình huống xấu nhất (Disaster Recovery).
- **Automation-first:** Bất cứ công việc nào lặp lại quá 2 lần đều cần được tự động hóa.
- **Immutable Infrastructure:** Tư duy hạ tầng bất biến – thay vì sửa trực tiếp trên server (SSH vào sửa cấu hình), hãy cập nhật code IaC và deploy lại server mới.

#### Kiến Trúc Kỹ Thuật

- **CI/CD Pipelines:** Hiểu rõ các bước để xây dựng một luồng ống chuẩn từ Source Code → Build → Test → Deploy.
- Tầm quan trọng của việc **phân tách môi trường** rõ ràng (Dev, Staging, Production) để cô lập rủi ro.
- Hiểu cách các công cụ quản lý cấu hình và hạ tầng hoạt động để đảm bảo tính nhất quán giữa các môi trường.

#### Chiến Lược Áp Dụng

- **Bắt đầu từ quy mô nhỏ:** Không cần áp dụng DevOps toàn diện ngay lập tức. Hãy bắt đầu từ việc tự động hóa khâu test, sau đó đến build, rồi mới đến deploy.
- Xây dựng **Post-mortem culture**: Khi thảm họa xảy ra, tập trung tìm nguyên nhân gốc rễ (Root Cause) thay vì đổ lỗi (Blameless culture).

### Ứng Dụng Vào Định Hướng Công Việc

- **Xây dựng CI/CD:** Áp dụng thiết lập pipeline tự động hóa cho các dự án Fullstack cá nhân để chuẩn bị hành trang trở thành kỹ sư Fullstack thực thụ, hiểu rõ vòng đời sản phẩm từ code đến deploy.
- **Áp dụng IaC vào AWS:** Thay vì tạo VPC, EC2 hay cấu hình mạng thủ công trên AWS Console, sẽ chuyển sang viết kịch bản tự động bằng CloudFormation hoặc Terraform.
- **Tối ưu hệ thống giám sát:** Tích hợp các hệ thống như Nagios hoặc AWS CloudWatch cho các máy chủ Linux (đặc biệt là CentOS) để theo dõi metrics mạng lưới và có cảnh báo sớm trước khi thảm họa xảy ra.
- **Quản trị hệ thống chuyên nghiệp:** Hạn chế thói quen SSH trực tiếp vào server để sửa lỗi nóng, thay vào đó sẽ quản lý cấu hình tập trung qua Git.

### Trải nghiệm trong event

Tham gia sự kiện **“THE HIDDEN ICEBERG OF A PROJECT: DEVOPS BEFORE DISASTER”** là một trải nghiệm thực tế và thức tỉnh, giúp tôi nhìn nhận lại cách vận hành các dự án công nghệ. Một số trải nghiệm nổi bật:

#### Bài học từ những "Thảm họa" thực tế
- Các diễn giả đã mổ xẻ những case study thực tế về các dự án bị sập hệ thống do coi thường "phần chìm của tảng băng". Điều này giúp tôi nhận ra hậu quả khôn lường của việc làm thủ công và thiếu quy trình kiểm thử hệ thống.

#### Tiếp cận kỹ thuật thực chiến
- Được giới thiệu luồng hoạt động thực tế của CI/CD pipeline và cách các kỹ sư DevOps tự động hóa hạ tầng. 
- Hiểu rõ hơn về tầm quan trọng của việc xây dựng hệ thống giám sát chủ động (observability) để "nhìn thấu" phần chìm của dự án, thay vì chỉ cấu hình server chạy là xong.

#### Tư duy văn hóa đội nhóm
- Nhận ra rằng rào cản lớn nhất của các dự án không nằm ở công nghệ mà ở sự thiếu giao tiếp giữa team Dev và team Ops. Workshop nhấn mạnh văn hóa chia sẻ trách nhiệm, một mindset cực kỳ quan trọng cho định hướng kỹ sư hệ thống/Fullstack sau này.

#### Kết luận rút ra
- Áp dụng văn hóa DevOps sớm sẽ giúp kiểm soát rủi ro, giảm thiểu downtime và tránh tình trạng "cháy nhà mới ra mặt chuột". 
- Tự động hóa và giám sát hệ thống mạng/máy chủ ngay từ đầu là khoản đầu tư sinh lời nhất về mặt thời gian và sự ổn định của bất kỳ dự án nào.

#### Một số hình ảnh khi tham gia sự kiện
*  (/images/event.jpg)
  (/images/enven2.jpg)
> 
