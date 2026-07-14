---
title: "Bản đề xuất"
date: 2026-07-04
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Đồ án Website Đặt Sân Thể Thao
## Giải pháp Triển khai Kiến trúc AWS High Availability & Scalable
### 1. Tóm tắt điều hành
Hệ thống Đặt sân thể thao (Sports Field Booking System) được thiết kế nhằm cung cấp một nền tảng web ổn định, bảo mật và có tính sẵn sàng cao cho người dùng. Nền tảng sử dụng kiến trúc AWS với việc tách biệt hoàn toàn Frontend (tĩnh) và Backend (động), tận dụng khả năng tự động mở rộng (Auto Scaling) trải dài trên nhiều Availability Zones (Multi-AZ). Giải pháp này giúp hệ thống luôn hoạt động trơn tru ngay cả trong các khung giờ cao điểm, tối ưu hóa chi phí vận hành và đảm bảo an toàn dữ liệu với Amazon RDS và các lớp bảo mật chuyên sâu như AWS WAF.

### 2. Tuyên bố vấn đề
### Vấn đề hiện tại
Các hệ thống đặt sân thể thao truyền thống thường gặp tình trạng quá tải, phản hồi chậm hoặc sập web trong những khung giờ vàng (ví dụ: 17h00 - 19h00). Việc lưu trữ tập trung trên một máy chủ duy nhất (Single Point of Failure) gây rủi ro mất dữ liệu, trong khi chi phí duy trì máy chủ cấu hình cao 24/7 lại gây lãng phí ngân sách khi hệ thống vắng khách.

### Giải pháp
Dự án áp dụng kiến trúc Cloud-native trên AWS. Frontend được lưu trữ tĩnh trên Amazon S3 và phân phối siêu tốc qua CloudFront. Trực tiếp xử lý logic Backend là cụm máy chủ EC2 (sử dụng Java Spring Boot) nằm trong Private Subnet, được quản lý tải bởi Application Load Balancer (ALB) và Auto Scaling Group. Cơ sở dữ liệu MySQL được lưu trữ trên Amazon RDS theo mô hình Multi-AZ (có bản sao lưu Standby) để chống lỗi. Hệ thống còn được giám sát liên tục bằng CloudWatch và cảnh báo qua SNS.

Lợi ích và hoàn vốn đầu tư (ROI)
Kiến trúc này mang lại thời gian hoạt động (Uptime) lên tới 99.9%, nâng cao trải nghiệm đặt sân của người dùng cuối. Hệ thống chỉ mở rộng tài nguyên tính toán (Scale-out) khi có lượng truy cập lớn và thu hẹp lại (Scale-in) khi rảnh rỗi, giúp tiết kiệm tối đa chi phí hạ tầng. Ngoài ra, việc bảo trì và nâng cấp cũng diễn ra liền mạch nhờ kiến trúc phân tán, không gây gián đoạn dịch vụ.

### 3. Kiến trúc giải pháp
Nền tảng áp dụng kiến trúc AWS kết hợp giữa Serverless (cho Frontend/Storage) và Auto-scaling Instances (cho Backend/Database) trên 2 Availability Zones (AZ A và AZ B).

### Luồng dữ liệu (Data Flow):
![Đồ án Website đặt sân thể thao](/images/2-Proposal/anh_kien_truc.png)

- **Truy cập & Bảo mật (1)**: Người dùng truy cập tên miền được phân giải bởi Route 53. Traffic đi qua CloudFront (CDN) và được kiểm duyệt bảo mật bởi AWS WAF.

- **Frontend (3)**: CloudFront lấy dữ liệu giao diện tĩnh (ReactJS/Vue/HTML...) từ FE Static S3 bucket.

- **Định tuyến Backend (2, 4)**: Các API requests đi qua Internet Gateway (IGW) đến Internet-facing ALB. ALB phân phối tải tới Target Group.

- **Xử lý Logic (5)**: Target Group điều hướng request đến các EC2 instances nằm trong Auto Scaling Group tại Private Subnet của AZ A hoặc AZ B. Các máy chủ này sử dụng NAT Gateway ở Public Subnet để truy cập Internet khi cần (ví dụ: gọi API thanh toán bên thứ ba).

- **Cơ sở dữ liệu (6)**: EC2 kết nối tới Amazon RDS MySQL (Primary) thông qua RDS Endpoint và Security Group. Dữ liệu được đồng bộ liên tục sang bản Standby ở AZ B (Multi-AZ) để đảm bảo an toàn và tính sẵn sàng cao.

- **Lưu trữ tĩnh Backend (7)**: Các tệp do người dùng tải lên (hình ảnh sân bãi, hóa đơn, avatar) được EC2 đẩy vào BE S3 bucket thông qua S3 Gateway Endpoint.

- **Giám sát & Cảnh báo (8)**: Trạng thái của RDS và hệ thống được CloudWatch thu thập, nếu có sự cố sẽ kích hoạt AWS SNS để gửi email cảnh báo cho quản trị viên.

### Dịch vụ AWS sử dụng chính

- **Amazon Route 53, CloudFront & WAF**: Quản lý DNS, tăng tốc độ tải trang và bảo vệ hệ thống khỏi các cuộc tấn công web phổ biến (như DDoS, SQL Injection).

- **Application Load Balancer (ALB) & Auto Scaling Group**: Cân bằng tải và tự động mở rộng/thu hẹp số lượng máy chủ EC2.

- **Amazon EC2**: Chạy ứng dụng Backend (Java Spring Boot, Hibernate).

- **Amazon RDS (MySQL, Multi-AZ)**: Quản lý cơ sở dữ liệu quan hệ, tự động failover khi có sự cố.

- **Amazon VPC, NAT Gateway, IGW**: Xây dựng mạng riêng ảo, tách biệt môi trường Public và Private để bảo mật tuyệt đối cho Backend và DB.

- **Amazon S3**: Lưu trữ Frontend tĩnh (FE Static S3) và tệp tin hệ thống (BE S3).

- **Amazon CloudWatch & SNS**: Giám sát tài nguyên, log và tự động thông báo qua Email.

### 4. Triển khai kỹ thuật
### Các giai đoạn triển khai
**Dự án được chia thành 4 giai đoạn chính để đưa ứng dụng lên AWS:**

- **Thiết lập Mạng & Lưu trữ cơ bản**: Cấu hình VPC, chia Subnets (Public/Private), thiết lập IGW, NAT Gateway và các S3 buckets. Đẩy code Frontend tĩnh lên S3.

- **Cấu hình Database & Server**: Khởi tạo Amazon RDS MySQL (Multi-AZ). Cấu hình Launch Template cho EC2 chứa môi trường chạy Java/Node.js, thiết lập Auto Scaling Group và ALB.

- **Triển khai Mạng biên & Bảo mật**: Kết nối Route 53 với tên miền, cấu hình CloudFront phân phối Frontend S3, và gắn AWS WAF để bảo vệ ALB/CloudFront.

- **Giám sát & Tối ưu**: Thiết lập các metrics giám sát trên CloudWatch, cấu hình SNS gửi email khi EC2 quá tải hoặc RDS gặp lỗi. Cấu hình CI/CD để tự động deploy code mới.

### Yêu cầu kỹ thuật

- **Frontend**: Build ra dạng file tĩnh (HTML/CSS/JS) tối ưu cho S3 static website hosting.

- **Backend**: Ứng dụng (vd: Java Spring Boot) phải theo chuẩn Stateless (không lưu session trên máy chủ, sử dụng JWT) để Auto Scaling hoạt động chính xác. Chạy qua port 80/8080 để ALB health check.

- **Database**: Sử dụng MySQL với kết nối Hibernate/JPA, cấu hình connection pool tối ưu để chịu tải từ nhiều EC2 instances cùng lúc.

### 5. Lộ trình & Mốc triển khai
- **Tuần 1**: Hoàn thiện Local & Khởi tạo Hạ tầng

    - Hoàn tất lập trình và kiểm thử chức năng hệ thống Đặt sân thể thao (giao diện tĩnh và backend Java Spring Boot) ở môi trường local.
    - Tạo tài khoản AWS, thiết kế mạng cốt lõi (VPC, Public/Private Subnets, Internet Gateway).

- **Tuần 2**: Triển khai Dữ liệu & Mạng biên

    - Khởi tạo và cấu hình cơ sở dữ liệu MySQL trên Amazon RDS.

    - Tải mã nguồn Frontend tĩnh lên S3 bucket và cấu hình phân phối nội dung tốc độ cao qua CloudFront.

- **Tuần 3**: Triển khai Backend & Mở rộng tự động

    - Đóng gói ứng dụng Backend, tạo Launch Template và thiết lập cụm máy chủ EC2 Auto Scaling.

    - Cấu hình Application Load Balancer (ALB) để định tuyến luồng truy cập an toàn vào Backend.

- **Tuần 4**: Hoàn thiện, Kiểm thử & Báo cáo

    - Tích hợp tên miền thực tế (Route 53) và thiết lập giám sát, cảnh báo hệ thống qua CloudWatch kết hợp SNS.

    - Thực hiện kiểm thử chịu tải (Load testing), rà soát tối ưu hóa chi phí và hoàn thành quyển báo cáo đồ án.

### 6. Ước tính ngân sách
Bạn có thể xem bảng ước tính ngân sách trên [AWS Pricing Calculator](https://calculator.aws/#/estimate?id=621f38b12a1ef026842ba2ddfe46ff936ed4ab01).  
Hoặc bạn có thể tải xuống [Budget Estimation File](../attachments/budget_estimation.pdf).

**Chi phí hạ tầng (Ước tính)**

 - Application Load Balancer (ALB): ~16.50 USD/tháng.

 - Amazon EC2 (2 instances t3.micro trong Auto Scaling): ~15.00 USD/tháng.

 - Amazon RDS (MySQL t3.micro, Multi-AZ): ~34.00 USD/tháng.

 - NAT Gateway (1 cái): ~32.00 USD/tháng.

 - Amazon S3 & CloudFront (Lưu lượng thấp): ~2.00 USD/tháng.

 - Route 53 (1 Hosted Zone): 0.50 USD/tháng.

 - AWS WAF, CloudWatch, SNS: Nằm trong Free Tier hoặc ~3.00 USD/tháng.

Tổng cộng: Khoảng 103.00 USD/tháng.

### 7. Đánh giá rủi ro
**Ma trận rủi ro**

 - Tấn công DDoS hoặc Web Exploit: Ảnh hưởng cao, xác suất trung bình.

 - Database quá tải do query phức tạp: Ảnh hưởng cao, xác suất cao (nếu lượng đặt sân đột biến).

 - Vượt ngân sách AWS (Cloud Shock): Ảnh hưởng cao, xác suất trung bình.

 - Chiến lược giảm thiểu

 - Bảo mật: Sử dụng AWS WAF để chặn IP độc hại, Rate Limiting trên CloudFront/ALB. Đặt DB và Backend trong Private Subnet, không cấp public IP.

 - Cơ sở dữ liệu: Tận dụng Read Replica (nếu cần mở rộng đọc), tối ưu index MySQL, sử dụng Hibernate Caching.

 - Chi phí: Cài đặt AWS Budgets để cảnh báo ngay lập tức nếu chi phí vượt quá ngưỡng 10$, 20$. Tắt các EC2 instance và RDS vào ban đêm khi không phát triển.

### 8. Kết quả mong đợi

**Về mặt kỹ thuật**

- Hệ thống hoạt động ổn định trên AWS.
- Có khả năng mở rộng khi lượng truy cập tăng.
- Đảm bảo tính sẵn sàng cao và an toàn dữ liệu.
- Tối ưu hiệu năng và chi phí vận hành.

**Về mặt học tập**

- Thông qua dự án, tôi có cơ hội vận dụng kiến thức về AWS Cloud, Java Spring Boot và triển khai hệ thống thực tế trên môi trường doanh nghiệp. Đây sẽ là nền tảng quan trọng để phát triển theo định hướng Backend Developer, Cloud Engineer hoặc DevOps Engineer trong tương lai.