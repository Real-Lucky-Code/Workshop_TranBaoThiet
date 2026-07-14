---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

## Mục tiêu tuần 11

* Hoàn thiện các nghiệp vụ cốt lõi của hệ thống đặt sân thể thao trực tuyến.
* Tích hợp cổng thanh toán trực tuyến và xây dựng hệ thống thông báo cho người dùng.
* Phát triển đầy đủ các chức năng dành cho Chủ sân (Owner) và Quản trị viên (Admin).
* Hoàn thiện giao diện người dùng và kiểm thử toàn bộ hệ thống trên môi trường phát triển.
* Chuẩn bị phiên bản ứng dụng sẵn sàng triển khai lên hạ tầng AWS trong tuần tiếp theo.

## Các công việc triển khai trong tuần

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | ---------------- | -------------- |
| 2 | - Phát triển và hoàn thiện nghiệp vụ đặt sân (Booking Workflow).<br>- Xây dựng cơ chế kiểm tra tính khả dụng của sân theo khung giờ, xử lý trùng lịch đặt, thời gian hoạt động và các khung giờ bị chặn.<br>- Phát triển chức năng lựa chọn các dịch vụ đi kèm và tính toán tổng giá trị đơn đặt sân trên môi trường localhost. | 29/06/2026 | 29/06/2026 | Không có tài liệu|
| 3 | - Tích hợp cổng thanh toán trực tuyến (VNPay/MoMo) vào hệ thống.<br>- Xây dựng quy trình tạo liên kết thanh toán, xử lý Redirect và Callback để cập nhật trạng thái giao dịch và đơn đặt sân.<br>- Hoàn thiện hệ thống thông báo (Notification) nhằm gửi trạng thái đơn đặt sân đến khách hàng và chủ sân sau khi giao dịch hoàn tất. | 30/06/2026 | 30/06/2026 | https://miniai.vn/tich-hop-thanh-toan-vnpay/ |
| 4 | - Hoàn thiện giao diện và nghiệp vụ dành cho Chủ sân (Owner Dashboard).<br>&emsp;+ Quản lý thông tin cơ sở thể thao và sân thi đấu.<br>&emsp;+ Duyệt hoặc từ chối các yêu cầu hủy đặt sân.<br>- Hoàn thiện giao diện và nghiệp vụ dành cho Quản trị viên (Admin Dashboard).<br>&emsp;+ Duyệt cơ sở thể thao mới đăng ký.<br>&emsp;+ Quản lý trạng thái tài khoản người dùng (Ban/Unban). | 01/07/2026 | 01/07/2026 | Không có tài liệu|
| 5 | - Hoàn thiện giao diện người dùng bằng Thymeleaf.<br>&emsp;+ Trang chi tiết cơ sở thể thao.<br>&emsp;+ Lịch sử đặt sân.<br>&emsp;+ Chức năng đánh giá và danh sách yêu thích.<br>- Thực hiện kiểm thử toàn diện (End-to-End Testing) các luồng chức năng từ Backend đến Frontend trên môi trường localhost.<br>- Hiệu chỉnh các lỗi phát sinh và hoàn thiện logic xử lý dữ liệu. | 02/07/2026 | 02/07/2026 | https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html |
| 6 | - Rà soát và hoàn thiện phiên bản ứng dụng hoạt động ổn định trên môi trường localhost.<br>- Kiểm tra lại toàn bộ các chức năng chính của hệ thống trước khi triển khai lên AWS.<br>- Tổng hợp tiến độ phát triển dự án trong tuần.<br>- Cập nhật Worklog tuần 11 lên báo cáo.<br>- Lập kế hoạch triển khai hệ thống lên hạ tầng AWS trong tuần tiếp theo. | 03/07/2026 | 03/07/2026 | Không có tài liệu |

## Kết quả đạt được tuần 11

### Về kiến thức

* Hiểu quy trình xây dựng và hoàn thiện các nghiệp vụ cốt lõi trong hệ thống đặt sân thể thao trực tuyến.
* Nắm được quy trình tích hợp cổng thanh toán trực tuyến và xử lý luồng giao dịch giữa hệ thống với dịch vụ thanh toán.
* Hiểu cơ chế xây dựng hệ thống thông báo và cập nhật trạng thái đơn đặt sân theo thời gian thực.
* Hiểu quy trình kiểm thử toàn diện (End-to-End Testing) trước khi triển khai hệ thống.

### Về phát triển hệ thống

* Hoàn thiện nghiệp vụ đặt sân với cơ chế kiểm tra lịch, xử lý xung đột và tính toán chi phí.
* Tích hợp thành công cổng thanh toán trực tuyến và xây dựng hệ thống thông báo cho người dùng.
* Hoàn thiện các chức năng dành cho Chủ sân (Owner) và Quản trị viên (Admin).
* Hoàn thiện giao diện người dùng và kết nối đầy đủ giữa Frontend, Backend và cơ sở dữ liệu.

### Về triển khai

* Kiểm thử toàn bộ các chức năng trên môi trường localhost và hiệu chỉnh các lỗi phát sinh.
* Hoàn thiện phiên bản ứng dụng ổn định, sẵn sàng cho quá trình triển khai lên hạ tầng AWS.
* Chuẩn bị kế hoạch triển khai và cấu hình môi trường AWS cho giai đoạn tiếp theo của dự án.

### Về kỹ năng

* Rèn luyện kỹ năng phát triển các nghiệp vụ phức tạp trong ứng dụng Spring Boot.
* Nâng cao khả năng tích hợp các dịch vụ bên thứ ba như cổng thanh toán trực tuyến.
* Thực hành kiểm thử tích hợp (Integration Testing) và kiểm thử toàn diện (End-to-End Testing) cho hệ thống.
* Hình thành quy trình hoàn thiện, kiểm thử và chuẩn bị triển khai một ứng dụng web trên nền tảng AWS Cloud.