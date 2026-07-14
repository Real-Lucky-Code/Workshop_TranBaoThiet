---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

## Mục tiêu tuần 6

* Hiểu cơ chế sao lưu và khôi phục dữ liệu trên AWS thông qua AWS Backup.
* Nắm được quy trình xây dựng Backup Plan, Backup Vault và quản lý Recovery Points.
* Tìm hiểu cơ chế giám sát và thông báo quá trình sao lưu bằng Amazon SNS.
* Hiểu mô hình lưu trữ Hybrid Cloud thông qua AWS Storage Gateway kết hợp với Amazon S3.
* Rèn luyện kỹ năng triển khai, kiểm thử và dọn dẹp tài nguyên nhằm tối ưu chi phí trong quá trình thực hành.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về AWS Backup và nội dung bài thực hành.<br>- Chuẩn bị hạ tầng triển khai.<br>&emsp;+ Tạo Amazon S3 Bucket phục vụ lưu trữ dữ liệu sao lưu.<br>&emsp;+ Triển khai hạ tầng bằng AWS CloudFormation để tạo Amazon EC2 Instance, Amazon SNS Topic và AWS Lambda Function.<br>- Xây dựng Backup Plan.<br>&emsp;+ Tạo Backup Vault.<br>&emsp;+ Cấu hình Backup Rules (tần suất sao lưu và thời gian lưu trữ).<br>&emsp;+ Gán tài nguyên vào Backup Plan thông qua Tags hoặc Resource ID. | 25/05/2026 | 25/05/2026 | https://000013.awsstudygroup.com/ |
| 3 | - Thiết lập hệ thống thông báo cho AWS Backup.<br>&emsp;+ Cấu hình Amazon SNS Topic.<br>&emsp;+ Đăng ký địa chỉ email nhận thông báo.<br>&emsp;+ Tích hợp AWS Backup với Amazon SNS để tự động gửi thông báo khi tác vụ sao lưu hoặc khôi phục hoàn thành.<br>- Thực hiện kiểm tra khả năng khôi phục dữ liệu.<br>&emsp;+ Kiểm tra các Recovery Points trong Backup Vault.<br>&emsp;+ Khôi phục tài nguyên từ Recovery Point.<br>&emsp;+ Kiểm tra và xác nhận tài nguyên sau khi khôi phục hoạt động bình thường.<br>- Dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành nhằm tránh phát sinh chi phí. | 26/05/2026 | 26/05/2026 | https://000013.awsstudygroup.com/ |
| 4 | - Tìm hiểu tổng quan về AWS Storage Gateway.<br>- Chuẩn bị môi trường triển khai Storage Gateway.<br>&emsp;+ Tạo Amazon S3 Bucket phục vụ lưu trữ dữ liệu.<br>&emsp;+ Khởi tạo Amazon EC2 Instance làm Storage Gateway.<br>&emsp;+ Tạo EC2 Key Pair và Security Group.<br>&emsp;+ Gắn thêm Amazon EBS Volume (150 GiB) làm Cache Storage cho Gateway.<br>&emsp;+ Kiểm tra và ghi nhận Public IP của EC2 Instance phục vụ cấu hình Gateway. | 27/05/2026 | 27/05/2026 | https://000024.awsstudygroup.com/ |
| 5 | - Khởi tạo AWS Storage Gateway.<br>&emsp;+ Kết nối Gateway thông qua Public IP của Amazon EC2 Instance.<br>&emsp;+ Cấu hình Cache Storage cho Gateway.<br>- Thiết lập quyền truy cập SMB.<br>- Tạo File Share và liên kết với Amazon S3 Bucket.<br>- Mount File Share từ máy tính On-premises để kiểm tra khả năng truy cập và đồng bộ dữ liệu. | 28/05/2026 | 28/05/2026 | https://000024.awsstudygroup.com/ |
| 6 | - Kiểm tra và dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành.<br>&emsp;+ Làm trống Amazon S3 Bucket.<br>&emsp;+ Xóa AWS Storage Gateway.<br>&emsp;+ Xóa Amazon EC2 Instance và các tài nguyên liên quan.<br>- Tổng hợp kiến thức đã học trong tuần.<br>- Cập nhật Worklog tuần 6 lên báo cáo.<br>- Lập kế hoạch học tập và thực hành cho tuần tiếp theo. | 29/05/2026 | 29/05/2026 | https://000024.awsstudygroup.com/3-cleanup/ |

## Kết quả đạt được tuần 6

### Về kiến thức

* Hiểu cơ chế sao lưu và khôi phục dữ liệu trên AWS thông qua AWS Backup.
* Nắm được quy trình xây dựng Backup Plan, Backup Vault và quản lý Recovery Points.
* Hiểu cơ chế gửi thông báo tự động của AWS Backup thông qua Amazon SNS.
* Hiểu mô hình lưu trữ Hybrid Cloud sử dụng AWS Storage Gateway kết hợp với Amazon S3.

### Về môi trường thực hành

* Triển khai thành công môi trường AWS Backup bằng AWS CloudFormation.
* Cấu hình Backup Plan và Backup Vault cho các tài nguyên trên AWS.
* Thiết lập thành công Amazon SNS Topic để nhận thông báo về các tác vụ sao lưu và khôi phục.
* Triển khai AWS Storage Gateway kết nối với Amazon S3 phục vụ lưu trữ dữ liệu.

### Về triển khai

* Thực hiện thành công quá trình sao lưu và khôi phục tài nguyên bằng AWS Backup.
* Kiểm tra các Recovery Points và xác nhận khả năng khôi phục dữ liệu.
* Tạo File Share và kết nối AWS Storage Gateway với Amazon S3.
* Mount File Share từ môi trường On-premises và kiểm tra khả năng truy cập dữ liệu.
* Dọn dẹp toàn bộ tài nguyên sau khi hoàn thành bài thực hành nhằm tránh phát sinh chi phí.

### Về kỹ năng

* Rèn luyện kỹ năng xây dựng chiến lược sao lưu và khôi phục dữ liệu trên AWS.
* Nâng cao kỹ năng cấu hình Amazon SNS phục vụ giám sát và thông báo tự động.
* Thực hành triển khai mô hình Hybrid Cloud thông qua AWS Storage Gateway.
* Hình thành quy trình triển khai, kiểm thử và dọn dẹp tài nguyên sau mỗi bài thực hành.