---
title: "Blog 2: AWS Interconnect chính thức phát hành rộng rãi"
date: 2026-04-07
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---


# AWS INTERCONNECT CHÍNH THỨC GA – ĐƠN GIẢN HÓA KẾT NỐI HYBRID CLOUD, MULTICLOUD VÀ LAST MILE

Trong tháng 4/2026, AWS đã chính thức phát hành rộng rãi (General Availability – GA) **AWS Interconnect** – một dịch vụ kết nối mạng được quản lý giúp đơn giản hóa việc kết nối giữa AWS với các nền tảng đám mây khác cũng như hạ tầng on-premises của doanh nghiệp.

Nếu trước đây, việc triển khai các kết nối mạng riêng thường yêu cầu nhiều tuần làm việc với nhà cung cấp viễn thông, cấu hình thủ công BGP, VLAN, Direct Connect hay VPN, thì giờ đây AWS Interconnect biến toàn bộ quy trình này thành một dịch vụ được quản lý hoàn toàn (turnkey managed service), cho phép người dùng triển khai chỉ với vài cú click trên AWS Console.

Đây được xem là một bước tiến quan trọng trong chiến lược mở rộng khả năng kết nối Hybrid Cloud, Multicloud và Last Mile của AWS.

## AWS Interconnect là gì?
AWS Interconnect là một dịch vụ kết nối mạng được quản lý (managed network connectivity service) giúp doanh nghiệp xây dựng các kết nối mạng riêng có tính bảo mật cao và độ sẵn sàng lớn giữa:
- AWS và các nền tảng Cloud khác (Interconnect – Multicloud).
- AWS và trung tâm dữ liệu hoặc văn phòng doanh nghiệp (Interconnect – Last Mile).

Toàn bộ lưu lượng được truyền trên hệ thống mạng backbone của AWS và các nhà cung cấp đối tác, không đi qua Internet công cộng, giúp tăng cường bảo mật, giảm độ trễ và mang lại hiệu năng ổn định.

## Hai năng lực kết nối cốt lõi

### AWS Interconnect – Multicloud
Đây là khả năng thiết lập kết nối Layer 3 riêng tư trực tiếp giữa Amazon VPC và các nền tảng Cloud khác. 
Hiện AWS hỗ trợ:
- **Google Cloud Platform** (đã GA).
- **Oracle Cloud Infrastructure (OCI)** – sẽ hỗ trợ trong năm 2026.
- **Microsoft Azure** – dự kiến hỗ trợ trong năm 2026.

Nhờ đó, dữ liệu giữa các Cloud được truyền hoàn toàn trên mạng backbone của các nhà cung cấp thay vì Internet công cộng, giúp tăng tính bảo mật và ổn định.

### AWS Interconnect – Last Mile
Đây là tính năng mới giúp đơn giản hóa việc kết nối từ trung tâm dữ liệu hoặc văn phòng doanh nghiệp đến AWS. 
Trước đây, doanh nghiệp thường phải phối hợp giữa nhiều bên như nhà cung cấp viễn thông, nhà cung cấp Cloud và đội ngũ vận hành mạng nội bộ để triển khai Direct Connect, cấu hình BGP, VLAN và kiểm thử đường truyền. Với AWS Interconnect, phần lớn quy trình này đã được tự động hóa.

Hiện AWS triển khai Last Mile thông qua các đối tác mạng như **Lumen Technologies** và sẽ tiếp tục mở rộng thêm nhiều đối tác khác trong tương lai. Người dùng chỉ cần lựa chọn:
- AWS Region
- Nhà cung cấp mạng
- Băng thông

Sau đó AWS sẽ tự động cấp phát kết nối, đồng thời toàn bộ quá trình cấu hình BGP, VLAN và mã hóa MACsec được xử lý phía sau mà người dùng gần như không cần thao tác thủ công. Những quy trình trước đây có thể mất nhiều tuần thì nay chỉ còn vài phút.

## Hệ sinh thái kết nối mở (Open Specification)
Một điểm rất đáng chú ý là AWS đã công bố đặc tả kỹ thuật (Open Specification) của AWS Interconnect trên GitHub theo giấy phép Apache 2.0.
Điều này cho phép các nhà cung cấp dịch vụ đám mây khác triển khai hỗ trợ AWS Interconnect, góp phần mở rộng hệ sinh thái Multicloud và giúp việc kết nối giữa các nền tảng Cloud trở nên linh hoạt hơn trong tương lai.

## Kiến trúc bảo mật và độ sẵn sàng cao (Maximum Resiliency)

![Hình 1: Kiến trúc AWS Interconnect – Multicloud với cấu hình Maximum Resiliency](/images/3-Blogs/hinh1_blog2.jpg)
*(Một kết nối logic được AWS ánh xạ thành nhiều kết nối vật lý thông qua hai Interconnection Facility nhằm tăng khả năng chịu lỗi, cân bằng tải và bảo mật)*

### Dự phòng 4 lớp (4-way Resiliency)
Khi khách hàng lựa chọn cấu hình Maximum Resiliency, AWS Interconnect sẽ tự động thiết lập bốn kết nối vật lý độc lập đi qua ít nhất hai Interconnection Facility.
Các kết nối này hoạt động theo cơ chế ECMP (Equal-Cost Multi-Path) để cân bằng tải và dự phòng.
Nếu một đường truyền hoặc một thiết bị gặp sự cố hay cần bảo trì, lưu lượng sẽ tự động chuyển sang đường còn lại mà không làm gián đoạn dịch vụ. Đối với AWS Interconnect – Last Mile, AWS cung cấp SLA lên đến 99.99% khi sử dụng cấu hình này.

### Mã hóa bằng MACsec
Toàn bộ dữ liệu được mã hóa bằng chuẩn IEEE 802.1AE MACsec ngay tại Layer 2. Việc mã hóa ở lớp liên kết dữ liệu giúp bảo vệ dữ liệu trong quá trình truyền tải mà gần như không ảnh hưởng đến hiệu năng.

### Điểm neo (Attach Point)
Phía AWS sử dụng Direct Connect Gateway (DXGW) làm điểm neo logic để kết nối vào AWS Global Backbone. Ở phía Cloud đối tác sẽ sử dụng các bộ định tuyến tương ứng (ví dụ Cloud Router của Google Cloud) để tiếp nhận và định tuyến lưu lượng.

## Quy trình triển khai với trải nghiệm Turnkey

![Hình 2: Quy trình triển khai AWS Interconnect](/images/3-Blogs/hinh2_blog2.jpg)
*(Người dùng tạo kết nối trên AWS Console, xác thực bằng Activation Key và Cloud Provider sẽ tự động hoàn tất việc cấp phát kết nối)*

- **Bước 1:** Khách hàng tạo một Interconnect mới trên AWS Management Console.
- **Bước 2:** AWS gửi yêu cầu tạo Interconnect đến nhà cung cấp Cloud, đồng thời sinh ra một Activation Key phục vụ quá trình xác thực.
- **Bước 3:** Khách hàng sử dụng Activation Key trên Console hoặc CLI của Cloud Provider để phê duyệt yêu cầu.
- **Bước 4:** Cloud Provider tự động hoàn tất việc cấp phát kết nối. Các cấu hình BGP và VLAN được thiết lập phía sau, sau đó hai hệ thống có thể giao tiếp với nhau ngay.

## Hiệu năng và khả năng giám sát
AWS Interconnect hỗ trợ băng thông từ 1 Gbps đến 100 Gbps và cho phép điều chỉnh trực tiếp trên AWS Console. Dịch vụ còn tích hợp với Amazon CloudWatch Network Synthetic Monitor để theo dõi:
- Latency (Độ trễ)
- Packet Loss (Tỷ lệ mất gói tin)
- Bandwidth Utilization (Mức độ sử dụng băng thông)

Nhờ đó, quản trị viên có thể giám sát chất lượng kết nối theo thời gian thực.

## Tối ưu chi phí (FinOps)
AWS cũng thay đổi cách tính phí so với các mô hình kết nối truyền thống. Thay vì tính phí truyền tải dữ liệu theo từng GB trên kết nối AWS Interconnect, khách hàng sử dụng **mức phí cố định theo băng thông và khu vực triển khai**. Điều này giúp doanh nghiệp dự báo chi phí tốt hơn, đặc biệt đối với các hệ thống AI, Big Data hoặc Data Lake có lưu lượng truyền tải lớn.

Từ tháng 5/2026, AWS cung cấp một kết nối AWS Interconnect – multicloud cục bộ (Tier 1) 500 Mbps miễn phí cho mỗi khách hàng, trên mỗi AWS Region và với mỗi CSP được hỗ trợ, giúp giảm đáng kể chi phí thử nghiệm và triển khai kết nối đa đám mây. Tuy nhiên, phía CSP vẫn áp dụng chính sách tính phí riêng của họ.

## Góc nhìn cá nhân
Sau khi tìm hiểu bài viết chính thức của AWS, mình nhận thấy AWS Interconnect không chỉ là một dịch vụ kết nối mạng mới mà còn phản ánh xu hướng **Network as a Service (NaaS)**, nơi việc triển khai và vận hành kết nối mạng ngày càng được đơn giản hóa và cung cấp dưới dạng dịch vụ.

Đồng thời, việc quản lý kết nối thông qua AWS Console, API và các quy trình tự động hóa cũng cho thấy hạ tầng mạng đang dần tiệm cận với cách tiếp cận của Infrastructure as Code (IaC) trong các hệ thống Cloud hiện đại.

Theo mình, với các hệ thống AI, Big Data, Data Lake cũng như các kiến trúc Hybrid Cloud và Multicloud, AWS Interconnect sẽ là một lựa chọn đáng cân nhắc nhờ khả năng kết nối riêng tư, bảo mật cao và triển khai nhanh chóng.

---
**Nguồn tham khảo:**
[AWS Blog – AWS Interconnect is now generally available with a new option to simplify last-mile connectivity](https://aws.amazon.com/vi/blogs/aws/aws-interconnect-is-now-generally-available-with-a-new-option-to-simplify-last-mile-connectivity/)