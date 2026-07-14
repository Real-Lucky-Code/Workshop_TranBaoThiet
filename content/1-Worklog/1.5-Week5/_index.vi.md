---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

## Mục tiêu tuần 5

* Hiểu cơ chế kết nối giữa nhiều Amazon VPC thông qua VPC Peering và AWS Transit Gateway.
* Nắm được quy trình cấu hình định tuyến và giao tiếp giữa các VPC trong cùng một Region.
* Hiểu vai trò của AWS CloudFormation trong việc tự động hóa quá trình triển khai hạ tầng.
* Thực hành cấu hình, kiểm tra và quản lý kết nối mạng giữa các VPC trên AWS.
* Rèn luyện kỹ năng triển khai, kiểm thử và dọn dẹp tài nguyên nhằm tối ưu chi phí trong quá trình thực hành.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về AWS CloudFormation và Amazon VPC Peering.<br>- Thực hiện các bước chuẩn bị cho bài thực hành.<br>&emsp;+ Khởi tạo AWS CloudFormation Template.<br>&emsp;+ Tạo Security Group.<br>&emsp;+ Khởi tạo Amazon EC2 Instances.<br>&emsp;+ Cập nhật Network ACL để đáp ứng yêu cầu kết nối giữa các VPC. | 18/05/2026 | 18/05/2026 | https://000019.awsstudygroup.com/ |
| 3 | - Thiết lập kết nối Amazon VPC Peering giữa các VPC.<br>- Cấu hình Route Tables cho VPC Peering.<br>- Thiết lập Cross-Peer DNS nhằm hỗ trợ phân giải tên miền giữa các VPC.<br>- Kiểm tra khả năng kết nối giữa các Amazon EC2 Instances thông qua VPC Peering.<br>- Dọn dẹp toàn bộ tài nguyên của bài thực hành VPC Peering nhằm tránh phát sinh chi phí. | 19/05/2026 | 19/05/2026 | https://000019.awsstudygroup.com/ |
| 4 | - Tìm hiểu tổng quan về AWS Transit Gateway.<br>- Chuẩn bị môi trường triển khai.<br>&emsp;+ Tạo EC2 Key Pair.<br>&emsp;+ Khởi tạo AWS CloudFormation Template.<br>&emsp;+ Khởi tạo AWS Transit Gateway. | 20/05/2026 | 20/05/2026 | https://000020.awsstudygroup.com/ |
| 5 | - Tạo các Transit Gateway Attachments để kết nối nhiều Amazon VPC.<br>- Cấu hình Transit Gateway Route Tables.<br>- Kiểm tra và xác nhận kết quả định tuyến giữa các VPC.<br>- Kiểm tra khả năng giao tiếp giữa các Amazon EC2 Instances thông qua AWS Transit Gateway. | 21/05/2026 | 21/05/2026 | https://000020.awsstudygroup.com/ |
| 6 | - Dọn dẹp toàn bộ tài nguyên của bài thực hành AWS Transit Gateway nhằm tránh phát sinh chi phí.<br>- Tổng hợp kiến thức đã học trong tuần.<br>- Cập nhật Worklog tuần 5 lên báo cáo.<br>- Lập kế hoạch học tập và thực hành cho tuần tiếp theo. | 22/05/2026 | 22/05/2026 | https://000020.awsstudygroup.com/7-cleanup/ |

## Kết quả đạt được tuần 5

### Về kiến thức

* Hiểu nguyên lý hoạt động của Amazon VPC Peering và AWS Transit Gateway.
* Nắm được quy trình cấu hình định tuyến giữa nhiều Amazon VPC thông qua Route Tables.
* Hiểu cơ chế phân giải tên miền giữa các VPC bằng Cross-Peer DNS.
* Hiểu vai trò của AWS CloudFormation trong việc tự động hóa triển khai hạ tầng AWS.

### Về môi trường thực hành

* Triển khai thành công môi trường thực hành sử dụng AWS CloudFormation.
* Thiết lập thành công kết nối Amazon VPC Peering giữa các Amazon VPC.
* Triển khai AWS Transit Gateway và kết nối nhiều Amazon VPC thông qua Transit Gateway Attachments.
* Kiểm tra thành công khả năng giao tiếp giữa các Amazon EC2 Instances thông qua các mô hình kết nối mạng.

### Về triển khai

* Cấu hình thành công Route Tables cho Amazon VPC Peering và AWS Transit Gateway.
* Thiết lập Cross-Peer DNS phục vụ việc phân giải tên miền giữa các Amazon VPC.
* Kiểm tra và xác nhận kết quả định tuyến giữa các VPC.
* Thực hiện dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành nhằm tránh phát sinh chi phí.

### Về kỹ năng

* Rèn luyện kỹ năng thiết kế và triển khai kết nối mạng giữa nhiều Amazon VPC.
* Thực hành sử dụng AWS CloudFormation để tự động hóa việc triển khai hạ tầng.
* Nâng cao kỹ năng cấu hình Route Tables, Network ACL và Transit Gateway.
* Hình thành quy trình triển khai, kiểm thử và dọn dẹp tài nguyên sau mỗi bài thực hành.