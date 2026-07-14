---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

## Mục tiêu tuần 8

* Hiểu vai trò của AWS Command Line Interface (AWS CLI) trong việc quản lý và tự động hóa các tác vụ trên AWS.
* Cài đặt và cấu hình AWS CLI để kết nối với tài khoản AWS thông qua Programmatic Access.
* Thực hành quản lý các dịch vụ AWS phổ biến bằng dòng lệnh như Amazon S3, Amazon SNS, IAM, Amazon VPC và Amazon EC2.
* Làm quen với việc chuyển từ thao tác trên AWS Management Console sang quản trị hạ tầng bằng Command-Line Interface.
* Rèn luyện kỹ năng kiểm tra, gỡ lỗi và xử lý các sự cố thường gặp khi sử dụng AWS CLI.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về AWS Command Line Interface (AWS CLI) và nội dung bài thực hành.<br>- Chuẩn bị môi trường sử dụng AWS CLI.<br>&emsp;+ Tạo IAM User và cấp Programmatic Access.<br>&emsp;+ Gán quyền truy cập cần thiết cho IAM User.<br>- Cài đặt AWS CLI trên máy tính cá nhân.<br>- Cấu hình AWS CLI bằng lệnh `aws configure`, bao gồm Access Key ID, Secret Access Key, Default Region và Output Format. | 08/06/2026 | 08/06/2026 | https://000011.awsstudygroup.com/ |
| 3 | - Thực hành quản lý và truy vấn tài nguyên AWS bằng AWS CLI.<br>- Thực hành làm việc với Amazon S3.<br>&emsp;+ Tạo và quản lý Amazon S3 Bucket.<br>&emsp;+ Upload và Download Objects.<br>&emsp;+ Đồng bộ dữ liệu bằng lệnh `aws s3 sync`.<br>- Thực hành làm việc với Amazon SNS.<br>&emsp;+ Tạo Amazon SNS Topic.<br>&emsp;+ Thiết lập Subscriptions.<br>&emsp;+ Publish Messages để kiểm tra hoạt động của SNS. | 09/06/2026 | 09/06/2026 | https://000011.awsstudygroup.com/ |
| 4 | - Thực hành quản lý IAM bằng AWS CLI.<br>&emsp;+ Tạo IAM User và IAM Group.<br>&emsp;+ Thêm IAM User vào Group.<br>&emsp;+ Gán IAM Policies.<br>&emsp;+ Tạo Access Keys cho IAM User.<br>- Thực hành quản lý hạ tầng mạng bằng AWS CLI.<br>&emsp;+ Tạo Amazon VPC.<br>&emsp;+ Tạo Subnet và Route Table.<br>&emsp;+ Tạo Internet Gateway và gắn vào Amazon VPC để thiết lập kết nối Internet. | 10/06/2026 | 10/06/2026 | https://000011.awsstudygroup.com/ |
| 5 | - Khởi tạo Amazon EC2 Instance bằng AWS CLI.<br>&emsp;+ Tạo EC2 Key Pair và Security Group.<br>&emsp;+ Khởi chạy Amazon EC2 Instance bằng lệnh `aws ec2 run-instances` với các tham số như Amazon Machine Image (AMI), Instance Type và Subnet ID.<br>&emsp;+ Kiểm tra trạng thái hoạt động bằng lệnh `aws ec2 describe-instances`.<br>- Thực hành xử lý sự cố (Troubleshooting).<br>&emsp;+ Kiểm tra và khắc phục các lỗi về Credentials, IAM Permissions và Region.<br>&emsp;+ Sử dụng tham số `--debug` để phân tích log và hỗ trợ xử lý sự cố. | 11/06/2026 | 11/06/2026 | https://000011.awsstudygroup.com/<br/>https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-troubleshooting.html |
| 6 | - Kiểm tra và dọn dẹp toàn bộ tài nguyên đã tạo bằng AWS CLI nhằm tránh phát sinh chi phí.<br>- Tổng hợp kiến thức đã học trong tuần.<br>- Cập nhật Worklog tuần 8 lên báo cáo.<br>- Lập kế hoạch học tập và thực hành cho tuần tiếp theo. | 12/06/2026 | 12/06/2026 | https://000011.awsstudygroup.com/11-cleanup/ |

## Kết quả đạt được tuần 8

### Về kiến thức

* Hiểu vai trò của AWS Command Line Interface (AWS CLI) trong việc quản lý và tự động hóa các tác vụ trên AWS.
* Nắm được quy trình cài đặt, cấu hình và xác thực AWS CLI thông qua IAM User và Programmatic Access.
* Hiểu cách quản lý các dịch vụ AWS phổ biến như Amazon S3, Amazon SNS, IAM, Amazon VPC và Amazon EC2 bằng dòng lệnh.
* Hiểu quy trình kiểm tra và xử lý các lỗi thường gặp khi sử dụng AWS CLI.

### Về môi trường thực hành

* Cài đặt và cấu hình thành công AWS CLI trên máy tính cá nhân.
* Thiết lập IAM User và Programmatic Access để sử dụng AWS CLI.
* Thực hành quản lý tài nguyên AWS thông qua Command-Line Interface thay cho AWS Management Console.
* Hoàn thiện môi trường phục vụ việc tự động hóa các tác vụ quản trị trên AWS.

### Về triển khai

* Thực hiện thành công các thao tác quản lý Amazon S3, Amazon SNS, IAM, Amazon VPC và Amazon EC2 bằng AWS CLI.
* Khởi tạo và quản lý Amazon EC2 Instance thông qua các câu lệnh AWS CLI.
* Thực hiện truy vấn, kiểm tra và quản lý tài nguyên AWS bằng các lệnh CLI.
* Áp dụng các kỹ thuật Troubleshooting để xử lý lỗi liên quan đến Credentials, IAM Permissions và Region.
* Dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành nhằm tránh phát sinh chi phí.

### Về kỹ năng

* Rèn luyện kỹ năng quản lý hạ tầng AWS bằng Command-Line Interface.
* Nâng cao kỹ năng sử dụng AWS CLI để tự động hóa các tác vụ quản trị trên AWS.
* Thực hành kiểm tra, phân tích log và xử lý sự cố bằng tham số `--debug`.
* Hình thành quy trình triển khai, kiểm thử và dọn dẹp tài nguyên theo các thực hành tốt trên AWS.