---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

## Mục tiêu tuần 12

* Triển khai hoàn chỉnh hệ thống đặt sân thể thao trực tuyến lên hạ tầng AWS Cloud.
* Điều chỉnh cấu hình ứng dụng để tương thích với môi trường triển khai thực tế.
* Tích hợp các dịch vụ AWS phục vụ lưu trữ, cơ sở dữ liệu và cân bằng tải.
* Kiểm thử, xác thực và tối ưu hệ thống sau khi triển khai.
* Hoàn thiện tài liệu dự án và tổng kết chương trình thực tập.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Triển khai hạ tầng AWS theo kiến trúc đã thiết kế.<br>- Cấu hình các thành phần mạng và bảo mật gồm VPC, Subnet, Route Table, Internet Gateway, NAT Gateway và Security Group.<br>- Khởi tạo Amazon EC2, Amazon RDS MySQL và Amazon S3 phục vụ môi trường triển khai của hệ thống. | 06/07/2026 | 06/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 3 | - Điều chỉnh cấu hình ứng dụng để phù hợp với môi trường AWS.<br>- Cập nhật cấu hình kết nối cơ sở dữ liệu, biến môi trường và các thông số triển khai.<br>- Tích hợp AWS SDK để ứng dụng lưu trữ và quản lý hình ảnh, tệp tin trực tiếp trên Amazon S3.<br>- Kiểm tra khả năng kết nối giữa ứng dụng và các dịch vụ AWS. | 07/07/2026 | 07/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Đóng gói ứng dụng bằng Maven và tạo file thực thi để triển khai.<br>- Triển khai ứng dụng lên Amazon EC2.<br>- Kiểm tra kết nối giữa EC2 và Amazon RDS.<br>- Rà soát Security Group và xác nhận các dịch vụ hoạt động ổn định sau khi triển khai. | 08/07/2026 | 08/07/2026 | https://docs.spring.io/spring-boot/index.html |
| 5 | - Thiết lập và cấu hình Application Load Balancer (ALB).<br>- Thiết lập Auto Scaling Group nhằm đảm bảo khả năng mở rộng và tính sẵn sàng cao của hệ thống.<br>- Kiểm tra Health Check của Load Balancer và hoạt động của Auto Scaling.<br>- Thực hiện kiểm thử toàn diện (End-to-End Testing) và xác thực các chức năng trên môi trường AWS Cloud.<br>- Hoàn thiện quá trình triển khai hệ thống lên AWS. | 09/07/2026 | 09/07/2026 | https://000016.awsstudygroup.com/ |
| 6 | - Rà soát toàn bộ hạ tầng đã triển khai nhằm tối ưu chi phí, bảo mật và tài nguyên sử dụng.<br>- Thực hiện kiểm tra cuối cùng (Final Validation) đối với toàn bộ hệ thống sau triển khai.<br>- Hoàn thiện tài liệu và báo cáo tổng kết dự án thực tập.<br>- Cập nhật Worklog tuần 12 lên báo cáo.<br>- Hoàn thành chương trình thực tập và tổng kết kết quả dự án. | 10/07/2026 | 10/07/2026 | Không có tài liệu |

## Kết quả đạt được tuần 12

### Về kiến thức

* Hiểu quy trình triển khai một ứng dụng Spring Boot từ môi trường phát triển lên hạ tầng AWS Cloud.
* Nắm được cách cấu hình ứng dụng để làm việc với các dịch vụ AWS như Amazon EC2, Amazon RDS và Amazon S3.
* Hiểu quy trình triển khai, kiểm thử và xác thực hệ thống sau khi đưa vào môi trường thực tế.
* Nắm được vai trò của Application Load Balancer và Auto Scaling Group trong việc nâng cao tính sẵn sàng và khả năng mở rộng của hệ thống.

### Về triển khai hạ tầng

* Triển khai thành công hạ tầng AWS theo kiến trúc đã thiết kế.
* Cấu hình và kết nối thành công giữa Amazon EC2, Amazon RDS và Amazon S3.
* Hoàn thiện cấu hình Application Load Balancer và Auto Scaling Group phục vụ quá trình vận hành hệ thống.
* Đưa ứng dụng lên môi trường AWS Cloud và đảm bảo hệ thống hoạt động ổn định.

### Về kiểm thử và vận hành

* Thực hiện kiểm thử toàn diện các chức năng trên môi trường triển khai thực tế.
* Xác nhận các luồng nghiệp vụ chính như đăng nhập, đặt sân, thanh toán và quản trị hoạt động đúng sau khi triển khai.
* Rà soát cấu hình bảo mật, tài nguyên và chi phí nhằm đảm bảo hệ thống sẵn sàng đưa vào vận hành.

### Về kỹ năng

* Rèn luyện kỹ năng triển khai ứng dụng Web lên môi trường AWS Cloud.
* Nâng cao khả năng cấu hình, tích hợp và quản lý các dịch vụ AWS trong một hệ thống hoàn chỉnh.
* Thực hành quy trình triển khai, kiểm thử và tối ưu hệ thống theo mô hình triển khai thực tế.
* Hoàn thiện kỹ năng xây dựng, triển khai và vận hành một ứng dụng Web trên nền tảng điện toán đám mây AWS.