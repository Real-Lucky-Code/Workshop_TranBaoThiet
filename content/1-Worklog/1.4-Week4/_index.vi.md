---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

## Mục tiêu tuần 4

* Hiểu quy trình triển khai ứng dụng web sử dụng Amazon EC2 kết hợp với Amazon RDS.
* Nắm được cách cấu hình kết nối giữa ứng dụng và cơ sở dữ liệu trong môi trường AWS.
* Tìm hiểu quy trình sao lưu và khôi phục dữ liệu bằng Amazon RDS Snapshots.
* Hiểu kiến trúc cân bằng tải với Elastic Load Balancing (ELB) và cơ chế mở rộng tài nguyên bằng Amazon EC2 Auto Scaling.
* Rèn luyện kỹ năng triển khai, giám sát và dọn dẹp tài nguyên nhằm tối ưu chi phí trong quá trình thực hành.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về Amazon RDS và nội dung bài thực hành.<br>- Chuẩn bị hạ tầng triển khai ứng dụng:<br>&emsp;+ Tạo Amazon VPC.<br>&emsp;+ Tạo Security Group cho Amazon EC2.<br>&emsp;+ Tạo Security Group cho Amazon RDS.<br>&emsp;+ Tạo DB Subnet Group phục vụ triển khai cơ sở dữ liệu. | 11/05/2026 | 11/05/2026 | https://000005.awsstudygroup.com/ |
| 3 | - Triển khai Amazon EC2 Instance.<br>&emsp;+ Chọn Amazon Machine Image (AMI).<br>&emsp;+ Chọn Instance Type.<br>&emsp;+ Cấu hình VPC, Subnet và Security Group.<br>&emsp;+ Khởi chạy và kiểm tra kết nối đến EC2 Instance.<br>- Triển khai Amazon RDS Database Instance.<br>&emsp;+ Lựa chọn Database Engine.<br>&emsp;+ Thiết lập thông tin xác thực (Credentials).<br>&emsp;+ Cấu hình DB Subnet Group và kết nối mạng.<br>&emsp;+ Kiểm tra trạng thái hoạt động của RDS Instance. | 12/05/2026 | 12/05/2026 | https://000005.awsstudygroup.com/ |
| 4 | - Triển khai ứng dụng web sử dụng Amazon EC2 và Amazon RDS.<br>&emsp;+ Cài đặt môi trường và các gói phần mềm cần thiết trên EC2.<br>&emsp;+ Thiết lập kết nối giữa ứng dụng và Amazon RDS.<br>&emsp;+ Kiểm tra ứng dụng hoạt động trên trình duyệt.<br>- Thực hiện sao lưu và khôi phục cơ sở dữ liệu.<br>&emsp;+ Tạo Amazon RDS Snapshot.<br>&emsp;+ Khôi phục Amazon RDS từ Snapshot.<br>- Dọn dẹp tài nguyên.<br>&emsp;+ Xóa Amazon RDS Database.<br>&emsp;+ Xóa Amazon EC2 Instance.<br>&emsp;+ Xóa DB Subnet Group, Security Group và Amazon VPC. | 13/05/2026 | 13/05/2026 | https://000005.awsstudygroup.com/ |
| 5 | - Tìm hiểu kiến trúc Elastic Load Balancing và Amazon EC2 Auto Scaling.<br>- Chuẩn bị hạ tầng triển khai Auto Scaling.<br>&emsp;+ Thiết lập hạ tầng mạng.<br>&emsp;+ Khởi chạy Amazon EC2 Instance.<br>&emsp;+ Khởi tạo Amazon RDS Database Instance.<br>&emsp;+ Thiết lập dữ liệu cho cơ sở dữ liệu.<br>&emsp;+ Triển khai Web Server.<br>&emsp;+ Chuẩn bị CloudWatch Metrics cho Predictive Scaling.<br>&emsp;+ Tạo Launch Template. | 14/05/2026 | 14/05/2026 | https://000006.awsstudygroup.com/ |
| 6 | - Thiết lập Elastic Load Balancer.<br>&emsp;+ Tạo Target Group.<br>&emsp;+ Tạo Application Load Balancer.<br>&emsp;+ Kiểm tra khả năng phân phối lưu lượng truy cập.<br>- Tạo Amazon EC2 Auto Scaling Group.<br>- Kiểm thử các chính sách Auto Scaling.<br>&emsp;+ Manual Scaling.<br>&emsp;+ Scheduled Scaling.<br>&emsp;+ Dynamic Scaling.<br>&emsp;+ Theo dõi Predictive Scaling thông qua CloudWatch Metrics.<br>- Dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành.<br>- Tổng hợp kiến thức đã học trong tuần.<br>- Cập nhật Worklog tuần 4 lên báo cáo.<br>- Lập kế hoạch học tập và thực hành cho tuần tiếp theo. | 15/05/2026 | 15/05/2026 | https://000006.awsstudygroup.com/ |

## Kết quả đạt được tuần 4

### Về kiến thức

* Hiểu quy trình triển khai ứng dụng web trên Amazon EC2 kết hợp với Amazon RDS.
* Nắm được cách cấu hình kết nối giữa ứng dụng và cơ sở dữ liệu trong môi trường AWS.
* Hiểu nguyên lý hoạt động của Elastic Load Balancing (ELB) và Amazon EC2 Auto Scaling.
* Hiểu quy trình sao lưu và khôi phục cơ sở dữ liệu bằng Amazon RDS Snapshots.

### Về môi trường thực hành

* Triển khai thành công Amazon EC2 Instance và Amazon RDS Database Instance.
* Thiết lập kết nối giữa ứng dụng web trên EC2 và cơ sở dữ liệu Amazon RDS.
* Triển khai thành công Elastic Load Balancer và Amazon EC2 Auto Scaling Group.
* Thiết lập môi trường thực hành phục vụ việc kiểm thử các chính sách mở rộng tài nguyên.

### Về triển khai

* Thực hiện thành công việc triển khai ứng dụng web trên Amazon EC2.
* Tạo và khôi phục cơ sở dữ liệu từ Amazon RDS Snapshots.
* Cấu hình Target Group, Launch Template và Application Load Balancer.
* Kiểm thử các chính sách Manual Scaling, Scheduled Scaling và Dynamic Scaling.
* Theo dõi và đánh giá Predictive Scaling thông qua CloudWatch Metrics.

### Về kỹ năng

* Rèn luyện kỹ năng triển khai ứng dụng nhiều tầng trên AWS.
* Thực hành cấu hình Elastic Load Balancer và Amazon EC2 Auto Scaling.
* Nâng cao kỹ năng sao lưu, khôi phục và quản lý cơ sở dữ liệu Amazon RDS.
* Hình thành quy trình triển khai, kiểm thử và dọn dẹp tài nguyên sau mỗi bài thực hành nhằm tối ưu chi phí.