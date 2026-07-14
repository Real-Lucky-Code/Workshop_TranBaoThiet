---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

## Mục tiêu tuần 2

* Hiểu cơ chế quản lý danh tính và phân quyền trên AWS thông qua dịch vụ AWS Identity and Access Management (IAM).
* Nắm được kiến thức nền tảng về Amazon VPC và các thành phần hạ tầng mạng trên AWS.
* Triển khai và quản lý Amazon EC2 trong môi trường VPC.
* Tìm hiểu nguyên lý hoạt động và quy trình cấu hình kết nối Site-to-Site VPN trên AWS.
* Rèn luyện kỹ năng triển khai, kiểm tra kết nối và dọn dẹp tài nguyên nhằm tối ưu chi phí trong quá trình thực hành.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về dịch vụ AWS Identity and Access Management (IAM).<br>- Nghiên cứu các thành phần chính gồm: IAM Users, IAM Groups, IAM Policies và IAM Roles.<br>- Thực hành tạo Admin Group và Admin User.<br>- Tạo Admin Role và OperatorUser.<br>- Cấu hình và thực hiện Switch Role để kiểm tra phân quyền.<br>- Dọn dẹp tài nguyên sau khi hoàn thành bài thực hành. | 27/04/2026 | 27/04/2026 |https://000002.awsstudygroup.com/ |
| 3 | - Tìm hiểu tổng quan về Amazon VPC và các thành phần bảo mật mạng.<br>- Thực hiện các bước chuẩn bị hạ tầng mạng:<br>&emsp;+ Tạo VPC.<br>&emsp;+ Tạo Public Subnet và Private Subnet.<br>&emsp;+ Tạo Internet Gateway.<br>&emsp;+ Cấu hình Route Table.<br>&emsp;+ Tạo Security Group.<br>&emsp;+ Kích hoạt VPC Flow Logs. | 28/04/2026 | 28/04/2026 | https://000003.awsstudygroup.com/ |
| 4 | - Triển khai Amazon EC2 Instance trong VPC.<br>- Kiểm tra khả năng kết nối đến EC2 Instance.<br>- Tạo NAT Gateway.<br>- Sử dụng Reachability Analyzer để kiểm tra luồng mạng.<br>- Tạo EC2 Instance Connect Endpoint.<br>- Quản lý EC2 thông qua AWS Systems Manager Session Manager.<br>- Thiết lập CloudWatch Monitoring và Alerting. | 29/04/2026 | 29/04/2026 | https://000003.awsstudygroup.com/4-createec2server/ |
| 5 | - Tìm hiểu và triển khai kết nối AWS Site-to-Site VPN.<br>- Chuẩn bị môi trường VPN:<br>&emsp;+ Tạo VPC dành cho VPN.<br>&emsp;+ Tạo EC2 làm Customer Gateway.<br>- Cấu hình Virtual Private Gateway, Customer Gateway và VPN Connection.<br>- Cấu hình Customer Gateway và tùy chỉnh AWS VPN Tunnel.<br>- Tìm hiểu các phương án VPN thay thế và hướng dẫn khắc phục sự cố (VPN Troubleshooting Guide). | 30/04/2026 | 30/04/2026 | https://000003.awsstudygroup.com/5-vpnsitetosite/ |
| 6 | - Kiểm tra và dọn dẹp toàn bộ tài nguyên đã tạo nhằm tránh phát sinh chi phí.<br>- Tổng hợp kiến thức đã học trong tuần.<br>- Cập nhật Worklog tuần 2 lên báo cáo.<br>- Lập kế hoạch học tập và thực hành cho tuần tiếp theo. | 01/05/2026 | 01/05/2026 | https://000003.awsstudygroup.com/6-cleanup/ |

## Kết quả đạt được tuần 2

### Về kiến thức

* Hiểu được cơ chế quản lý danh tính và phân quyền trên AWS thông qua dịch vụ IAM.
* Nắm được vai trò và cách sử dụng của IAM User, IAM Group, IAM Policy và IAM Role.
* Hiểu kiến trúc mạng cơ bản của Amazon VPC và chức năng của các thành phần như VPC, Subnet, Internet Gateway, Route Table và Security Group.
* Hiểu nguyên lý hoạt động của NAT Gateway, Reachability Analyzer và Site-to-Site VPN trong việc kết nối và quản lý hạ tầng mạng trên AWS.

### Về môi trường thực hành

* Triển khai thành công môi trường mạng cơ bản trên AWS với Amazon VPC.
* Khởi tạo và quản lý Amazon EC2 Instance trong môi trường VPC.
* Thiết lập và sử dụng AWS Systems Manager Session Manager để quản lý EC2.
* Thiết lập CloudWatch Monitoring và Alerting để giám sát tài nguyên.

### Về triển khai và bảo mật

* Thực hiện tạo và quản lý IAM User, IAM Group và IAM Role.
* Cấu hình và kiểm tra cơ chế Switch Role để xác minh quyền truy cập.
* Triển khai môi trường Site-to-Site VPN cơ bản giữa AWS và hệ thống mô phỏng Customer Gateway.
* Hiểu quy trình cấu hình VPN Tunnel và các phương pháp xử lý sự cố cơ bản.

### Về kỹ năng

* Rèn luyện kỹ năng thiết kế và triển khai hạ tầng mạng cơ bản trên AWS.
* Thực hành kiểm tra kết nối và phân tích luồng mạng bằng Reachability Analyzer.
* Hình thành quy trình triển khai, kiểm tra và dọn dẹp tài nguyên sau mỗi bài thực hành nhằm tối ưu chi phí.
* Nâng cao khả năng tự học thông qua tài liệu hướng dẫn và các bài thực hành của chương trình.