---
title: "Blog 3: Cách AWS DevOps Agent tìm nguyên nhân gốc rễ"
date: 2026-04-07
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# CÁCH AWS DEVOPS AGENT SỬ DỤNG TƯ DUY ĐA TÁC TỬ ĐỂ TÌM NGUYÊN NHÂN GỐC RỄ

Thiên kiến xác nhận (Confirmation bias) là một trong những lý do phổ biến nhất khiến việc điều tra sự cố kéo dài hơn mức cần thiết. Một kỹ sư trực ban (on-call) nhận được cảnh báo, đưa ra một giả thuyết dựa trên kinh nghiệm, tìm thấy một mảnh bằng chứng phù hợp và... dừng việc tìm kiếm. Trong khi đó, nguyên nhân gốc rễ (root cause) thực sự — có thể nằm ở một dịch vụ khác, một tín hiệu khác, hoặc một khung thời gian khác — lại tiếp tục bị bỏ ngỏ.

Các hệ thống phân tán hiện đại không thiếu dữ liệu đo lường từ xa (telemetry). Thứ chúng thiếu là khả năng suy luận (reasoning) — khả năng tạo ra nhiều lời giải thích cùng lúc, chủ động phản biện từng giả thuyết và chỉ kết luận khi có bằng chứng hỗ trợ một cách xác đáng.

AWS DevOps Agent, một tác tử tự trị, giải quyết vấn đề này bằng kiến trúc đa tác tử (multi-agent architecture). Nó chia nhỏ các quy trình xử lý sự cố thành các năng lực chuyên biệt. Tuy nhiên, điểm làm nên sự khác biệt của tác tử này không chỉ nằm ở việc tìm kiếm dữ liệu, mà ở khả năng hiểu bối cảnh kiến trúc (architectural context) — tài nguyên nào đang tồn tại, chúng liên kết ra sao và thay đổi thế nào sau mỗi lần triển khai (deployment).

Bài viết này sẽ đi sâu vào vòng đời điều tra sự cố để xem cách AWS DevOps Agent suy luận và chuyển mình từ một "hộp đen" thành một thành viên on-call đáng tin cậy.

## 1. Vòng đời Sự cố (The Incident Lifecycle)

AWS DevOps Agent tổ chức quy trình phản hồi sự cố thành các năng lực chuyên biệt, phản ánh cách làm việc của các đội ngũ SRE (Site Reliability Engineering) hàng đầu. Tất cả đều chia sẻ một nền tảng chung:

*   **Triage (Phân loại):** Tương quan hóa các tín hiệu đầu vào và làm phong phú bối cảnh điều tra. Tối ưu hóa cho tốc độ.
*   **Investigation (Điều tra):** Phân tích nguyên nhân gốc rễ chuyên sâu với việc tạo giả thuyết song song và xác thực bằng chứng phản bác. Đây là cỗ máy suy luận cốt lõi.
*   **Mitigation (Giảm thiểu):** Tạo ra các hành động khắc phục tức thời dựa trên nguyên nhân gốc rễ đã tìm ra.
*   **Prevention (Ngăn ngừa):** Phân tích các mẫu (patterns) từ các sự cố trong quá khứ để ngăn chặn tương lai.

Tất cả các năng lực này đều phụ thuộc vào một nền tảng quan trọng: Đồ thị cấu trúc ứng dụng (Topology graph).

![Hình 1: Vòng đời phản hồi sự cố của AWS DevOps Agent](/images/3-Blogs/hinh1_blog3.jpg)

## 2. Topology: Nền tảng cốt lõi

Trước khi có thể điều tra sự cố, tác tử cần hiểu kiến trúc của bạn — không chỉ là danh sách tài nguyên tĩnh, mà là một bản đồ sống động về cách chúng giao tiếp và liên kết với mã nguồn.

Hệ thống topology xây dựng sự hiểu biết này thông qua:
*   Phân tích AWS CloudFormation (bao gồm cả AWS CDK).
*   Khám phá tài nguyên qua AWS Resource Explorer.
*   Lập bản đồ hành vi thời gian thực qua CloudWatch Application Signals và các nền tảng bên thứ ba (Datadog, Dynatrace).
*   Tích hợp CI/CD (GitHub Actions, GitLab) để liên kết với quá trình triển khai.

Kết quả là một cấu trúc topology được học hỏi liên tục. Khi tác tử cần truy xuất lỗi hoặc đánh giá phạm vi ảnh hưởng (blast radius), nó sẽ dựa vào mạng lưới này. Mọi thứ hoạt động trong một **Agent Space** — một không gian độc lập được khoanh vùng cho từng team hoặc ứng dụng cụ thể.

![Hình 2: Cấu trúc Topology và Agent Space](/images/3-Blogs/hinh2_blog3.jpg)

## 3. Triage: Phân loại và Tương quan nhanh chóng

Khi một sự cố xảy ra (từ CloudWatch, PagerDuty, hay Grafana), Triage là bước đầu tiên được kích hoạt. Nó được tối ưu hóa cho tốc độ xử lý âm lượng lớn trong thời gian ngắn.

Tính năng quan trọng nhất của Triage là **sự tương quan (correlation)**. Tác tử tự động liên kết các cảnh báo (alarms) liên quan để biết khi nào chúng bắt nguồn từ cùng một sự kiện. Điều này giúp giảm thiểu độ nhiễu và gom các mảnh bằng chứng lại thành một cuộc điều tra toàn diện. Tuy nhiên, quyền kiểm soát cuối cùng vẫn thuộc về con người — các kỹ sư hoàn toàn có thể gỡ liên kết (unlink) nếu họ cho rằng các cảnh báo đó không liên quan.

## 4. Investigation: Cỗ máy Suy luận (The Reasoning Engine)

Đây là trọng tâm của AWS DevOps Agent, tuân theo một phương pháp luận có cấu trúc chặt chẽ.

### Thu thập ngữ cảnh và Dữ liệu
Tác tử bắt đầu bằng hai câu hỏi: *Cái gì bị ảnh hưởng?* và *Cái gì mới thay đổi?* Nó lập bản đồ phạm vi ảnh hưởng từ các tài nguyên bị lỗi, kiểm tra các hoạt động triển khai CI/CD gần đây, truy xuất các số liệu thống kê (metrics), nhật ký (logs) từ Splunk/Datadog và phân tích lịch sử cấu hình.

### Tạo Giả thuyết (Hypothesis Generation)
Thay vì bám vào một giả thuyết duy nhất, tác tử tạo ra nhiều giả thuyết cạnh tranh cùng lúc:
*   **Nhận diện mẫu:** Triệu chứng giống với một lỗi từng xảy ra.
*   **Phát hiện bất thường:** Một chỉ số vốn ổn định đột nhiên sai lệch.
*   **Tương quan thời gian:** Các lần triển khai (deployments) hoặc giới hạn tài nguyên (CPU, connection pools) trùng khớp với thời điểm xảy ra sự cố.

### Thu thập bằng chứng và Xác định Root Cause
Tác tử xác thực nhiều giả thuyết song song. 

**Ví dụ thực tế:** Dịch vụ thanh toán (checkout) của một trang e-commerce bị tăng độ trễ (latency). Tác tử đưa ra 3 giả thuyết:
1.  Có thay đổi cấu hình trước đó 20 phút.
2.  Cổng thanh toán (payment gateway) phản hồi chậm.
3.  Connection pool của Database sắp cạn.

Thay vì chạy theo một hướng, nó kiểm tra cả 3: Thay đổi cấu hình chỉ là về log *(loại)*. Cổng thanh toán chậm sau khi độ trễ checkout bắt đầu -> Đây là triệu chứng, không phải nguyên nhân *(loại)*. Connection pool đạt 94% ngay thời điểm bắt đầu lỗi -> **Đó chính là root cause.**

![Hình 3: Quá trình tạo và xác thực giả thuyết song song](/images/3-Blogs/hinh3_blog3.jpg)

## 5. Mitigation: An toàn là trên hết (Safe by default)

Sau khi tìm ra nguyên nhân, tác tử tạo ra một bản kế hoạch giảm thiểu (mitigation plan) bao gồm: Chiến lược khắc phục, quy trình từng bước, kiểm tra xác thực, tiêu chí thành công và quy trình rollback (hoàn tác).

**Điểm đặc biệt:** AWS DevOps Agent chỉ tạo kế hoạch chứ *không tự động thực thi* các hành động thay đổi hệ thống. Quyền "ghi" (write) của nó bị giới hạn ở việc tạo ticket. Các kỹ sư trực ban sẽ là người xem xét bản kế hoạch, đánh giá tầm ảnh hưởng thông qua Topology và đưa ra quyết định cuối cùng. Điều này đảm bảo an toàn tuyệt đối khi hệ thống đang chịu áp lực lớn.

## 6. Prevention: Từ thụ động đến chủ động

Giá trị lớn nhất của tác tử nằm ở việc xâu chuỗi các sự cố. Tính năng Prevention nhóm các sự cố đã qua có chung nguyên nhân gốc rễ, dù triệu chứng bề ngoài có vẻ khác nhau.

Dựa trên các phân tích này, hệ thống sẽ đưa ra những **khuyến nghị nhắm mục tiêu (targeted recommendations)** về:
*   Tối ưu hóa giám sát (Observability).
*   Kiểm thử và xác thực.
*   Các mẫu mã nguồn phục hồi (code resilience) như retry logic hay circuit breakers.
*   Tối ưu hóa hạ tầng và quy chuẩn quản trị.

Kỹ sư có thể thêm các khuyến nghị này vào backlog hoặc từ chối chúng bằng ngôn ngữ tự nhiên để AI học hỏi cho những lần sau.

![Hình 4: Đưa ra các khuyến nghị Prevention](/images/3-Blogs/hinh4_blog3.jpg)

## 7. Kết luận

AWS DevOps Agent kết nối các năng lực này thành một bánh đà vận hành liên tục. Đồ thị Topology mang lại sự hiểu biết về kiến trúc -> Investigation dựa vào đó để truy xuất lỗi -> Mitigation dùng để đánh giá rủi ro -> Các phát hiện tiếp tục được đưa vào Prevention để ngăn sự cố lặp lại.

Bằng cách ghi lại toàn bộ quá trình suy luận vào một nhật ký bất biến (immutable journal) và bảo tồn kiến thức vận hành ngay cả khi có sự thay đổi về nhân sự, AWS DevOps Agent giúp các kỹ sư trực ban giảm bớt áp lực, đưa ra quyết định chính xác hơn và tự tin hơn mỗi khi hệ thống gặp sự cố lúc nửa đêm.

---
**Nguồn tham khảo:** 
[How AWS DevOps Agent uses multi-agent reasoning to find root causes](https://aws.amazon.com/vi/blogs/devops/how-aws-devops-agent-uses-multi-agent-reasoning-to-find-root-causes/)