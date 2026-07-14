---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

## Mục tiêu tuần 10

* Hoàn thiện thiết kế kiến trúc và khởi tạo môi trường phát triển cho dự án.
* Xây dựng nền tảng Backend theo mô hình Spring Boot với kiến trúc phân tầng.
* Thiết kế mô hình dữ liệu, xây dựng các Entity và tầng truy cập cơ sở dữ liệu.
* Triển khai cơ chế xác thực (Authentication) và phân quyền (Authorization) bằng Spring Security.
* Phát triển các chức năng nghiệp vụ đầu tiên và tích hợp giao diện bằng Thymeleaf.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Rà soát, chỉnh sửa và hoàn thiện sơ đồ kiến trúc triển khai dự án trên AWS Cloud.<br>- Khởi tạo mã nguồn dự án và cấu hình môi trường phát triển với Java 21, Spring Boot 4 và Maven.<br>- Thiết lập kết nối cơ sở dữ liệu MySQL và cấu hình các thông số ban đầu của ứng dụng. | 22/06/2026 | 22/06/2026 | https://docs.spring.io/spring-boot/index.html |
| 3 | - Xây dựng tầng dữ liệu (Data Layer) của hệ thống.<br>- Thiết kế và xây dựng các Entity cốt lõi gồm User, Facility, Field, Booking và ExtraService.<br>- Thiết lập mối quan hệ giữa các Entity theo mô hình cơ sở dữ liệu.<br>- Xây dựng tầng Repository bằng Spring Data JPA và tầng Service để xử lý nghiệp vụ và tương tác với cơ sở dữ liệu. | 23/06/2026 | 23/06/2026 | https://docs.spring.io/spring-data/jpa/reference/index.html |
| 4 | - Xây dựng cơ chế xác thực và phân quyền bằng Spring Security.<br>- Cấu hình Authentication và Authorization cho hệ thống.<br>- Phát triển chức năng đăng ký, đăng nhập và phân quyền cho các vai trò User, Owner và Admin.<br>- Kiểm tra hoạt động của cơ chế bảo mật đối với các chức năng cơ bản. | 24/06/2026 | 24/06/2026 | https://docs.spring.io/spring-security/reference/index.html |
| 5 | - Phát triển tầng nghiệp vụ (Business Layer) cho chức năng quản lý cơ sở thể thao.<br>- Xây dựng API và Business Logic cho việc tạo cơ sở, quản lý sân thi đấu và các chức năng quản trị cơ bản.<br>- Tích hợp giao diện người dùng bằng Thymeleaf cho các trang đăng nhập, đăng ký và quản lý cơ sở.<br>- Kiểm tra luồng xử lý giữa giao diện, tầng nghiệp vụ và cơ sở dữ liệu. | 25/06/2026 | 25/06/2026 | Không có tài liệu |
| 6 | - Kiểm tra, hiệu chỉnh và hoàn thiện các chức năng đã triển khai trong tuần.<br>- Kiểm thử các chức năng đăng ký, đăng nhập, phân quyền và quản lý cơ sở.<br>- Tổng hợp tiến độ phát triển dự án.<br>- Cập nhật Worklog tuần 10 lên báo cáo.<br>- Lập kế hoạch triển khai các chức năng đặt sân và thanh toán trực tuyến cho tuần tiếp theo. | 26/06/2026 | 26/06/2026 | Không có tài liệu |

## Kết quả đạt được tuần 10

### Về kiến thức

* Hiểu quy trình xây dựng ứng dụng Spring Boot theo mô hình kiến trúc phân tầng (Layered Architecture).
* Nắm được cách tổ chức các tầng Entity, Repository, Service và Controller trong ứng dụng.
* Hiểu cơ chế xác thực (Authentication) và phân quyền (Authorization) bằng Spring Security.
* Nắm được quy trình kết nối và thao tác với cơ sở dữ liệu MySQL thông qua Spring Data JPA.

### Về thiết kế hệ thống

* Hoàn thiện sơ đồ kiến trúc triển khai của dự án trên AWS Cloud.
* Xây dựng mô hình dữ liệu và các Entity cốt lõi của hệ thống.
* Thiết lập mối quan hệ giữa các Entity làm nền tảng cho việc phát triển các chức năng nghiệp vụ.

### Về triển khai

* Khởi tạo thành công dự án Spring Boot và cấu hình môi trường phát triển.
* Xây dựng hoàn chỉnh tầng Repository và Service phục vụ truy cập cơ sở dữ liệu.
* Triển khai chức năng đăng ký, đăng nhập và phân quyền cho các vai trò User, Owner và Admin.
* Phát triển các chức năng quản lý cơ sở thể thao và tích hợp giao diện bằng Thymeleaf.
* Kiểm thử và hoàn thiện các chức năng nền tảng trước khi triển khai các nghiệp vụ phức tạp hơn.

### Về kỹ năng

* Rèn luyện kỹ năng phát triển ứng dụng Backend bằng Spring Boot.
* Nâng cao khả năng thiết kế mô hình dữ liệu và xây dựng kiến trúc phần mềm theo mô hình phân tầng.
* Thực hành tích hợp cơ sở dữ liệu, bảo mật và giao diện trong cùng một hệ thống.
* Hình thành quy trình phát triển, kiểm thử và hoàn thiện chức năng theo từng giai đoạn của dự án.