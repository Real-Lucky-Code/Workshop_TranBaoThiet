---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

## Mục tiêu tuần 9

* Xác định đề tài, phạm vi và định hướng triển khai dự án thực tế trong chương trình thực tập.
* Phân tích yêu cầu nghiệp vụ và các chức năng cốt lõi của hệ thống.
* Lựa chọn kiến trúc công nghệ (Technology Stack) và các dịch vụ AWS phù hợp với yêu cầu của dự án.
* Thiết kế kiến trúc tổng thể (High-Level Architecture) làm nền tảng cho quá trình triển khai hệ thống.
* Chuẩn bị kế hoạch xây dựng hạ tầng AWS và phát triển ứng dụng trong các tuần tiếp theo.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Xác định đề tài và phạm vi dự án: **Hệ thống đặt sân thể thao trực tuyến**.<br>- Phân tích các chức năng chính của hệ thống gồm tìm kiếm sân, đặt lịch, quản lý cơ sở thể thao và thanh toán trực tuyến.<br>- Lựa chọn kiến trúc công nghệ (Technology Stack) cho dự án gồm Java 21, Spring Boot 4 (Spring MVC, Spring Security), Thymeleaf và MySQL. | 15/06/2026 | 15/06/2026 | Không có tài liệu |
| 3 | - Phân tích yêu cầu nghiệp vụ của hệ thống.<br>- Xây dựng các luồng hoạt động chính gồm:<br>&emsp;+ Luồng đặt sân.<br>&emsp;+ Luồng thanh toán trực tuyến (VNPay/MoMo).<br>&emsp;+ Luồng quản trị dành cho Admin và Chủ sân.<br>- Xác định các yêu cầu về khả năng mở rộng (Scalability), bảo mật (Security) và tính sẵn sàng cao (High Availability) làm cơ sở cho việc thiết kế hạ tầng AWS. | 16/06/2026 | 16/06/2026 | Không có tài liệu|
| 4 | - Thiết kế kiến trúc hạ tầng AWS cho dự án.<br>- Lựa chọn các dịch vụ mạng và tính toán gồm Amazon VPC (Public/Private Subnets, Internet Gateway, NAT Gateway), Amazon EC2, Auto Scaling Group và Application Load Balancer (ALB).<br>- Lựa chọn Amazon RDS for MySQL (Primary/Standby) và Amazon S3 để lưu trữ Static Assets thông qua S3 Gateway Endpoint.<br>- Lựa chọn AWS WAF, Amazon CloudWatch và Amazon SNS nhằm tăng cường bảo mật, giám sát và cảnh báo hệ thống. | 17/06/2026 | 17/06/2026 | https://aws.amazon.com/vi/what-is/architecture-diagramming/ |
| 5 | - Thiết kế sơ đồ kiến trúc tổng thể (High-Level Architecture) của hệ thống trên nền tảng AWS Cloud.<br>- Xác định luồng truy cập của người dùng và luồng giao tiếp giữa các thành phần trong hệ thống.<br>- Đánh giá khả năng đáp ứng các yêu cầu về hiệu năng, khả năng mở rộng, bảo mật và tính sẵn sàng của kiến trúc đã thiết kế. | 18/06/2026 | 18/06/2026 | https://youtu.be/l8isyDe-GwY?si=FO9X7Zn1cscmuB1L |
| 6 | - Rà soát, đánh giá và hoàn thiện sơ đồ kiến trúc của hệ thống.<br>- Thống nhất phương án triển khai hạ tầng AWS cho dự án.<br>- Cập nhật Worklog tuần 9 lên báo cáo.<br>- Lập kế hoạch khởi tạo hạ tầng AWS và phát triển mã nguồn cho tuần tiếp theo. | 19/06/2026 | 19/06/2026 | Không có tài liệu|

## Kết quả đạt được tuần 9

### Về kiến thức

* Hiểu quy trình phân tích yêu cầu và thiết kế kiến trúc cho một dự án triển khai trên nền tảng AWS.
* Nắm được vai trò của các dịch vụ AWS trong việc xây dựng hệ thống web đáp ứng các yêu cầu về hiệu năng, khả năng mở rộng, bảo mật và tính sẵn sàng.
* Hiểu mối quan hệ giữa tầng mạng, tầng ứng dụng, cơ sở dữ liệu và các dịch vụ giám sát trong kiến trúc AWS.

### Về thiết kế hệ thống

* Hoàn thành việc xác định phạm vi, chức năng và kiến trúc công nghệ cho dự án.
* Phân tích các luồng nghiệp vụ chính của hệ thống làm cơ sở cho quá trình triển khai.
* Hoàn thành thiết kế sơ đồ kiến trúc tổng thể (High-Level Architecture) của hệ thống trên AWS Cloud.
* Xác định các dịch vụ AWS sẽ sử dụng trong toàn bộ quá trình phát triển dự án.

### Về triển khai

* Lựa chọn phương án triển khai hạ tầng AWS phù hợp với yêu cầu của hệ thống.
* Hoàn thiện bản thiết kế kiến trúc và chuẩn bị kế hoạch triển khai hạ tầng cho giai đoạn phát triển.
* Xây dựng nền tảng ban đầu phục vụ quá trình phát triển và triển khai ứng dụng trong các tuần tiếp theo.

### Về kỹ năng

* Rèn luyện kỹ năng phân tích yêu cầu nghiệp vụ và thiết kế kiến trúc hệ thống.
* Nâng cao khả năng lựa chọn công nghệ và dịch vụ AWS phù hợp với bài toán thực tế.
* Hình thành tư duy thiết kế hệ thống theo hướng đáp ứng các yêu cầu về khả năng mở rộng, bảo mật và tính sẵn sàng cao.
* Rèn luyện kỹ năng lập kế hoạch và chuẩn bị trước khi triển khai một dự án trên nền tảng AWS Cloud.