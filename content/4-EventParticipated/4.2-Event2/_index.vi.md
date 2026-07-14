---
title: "Event 2"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# BÀI THU HOẠCH: AWS COMMUNITY MEETUP (06/06/2026)

### Mục Đích Của Sự Kiện

- Khám phá các công nghệ điện toán đám mây hiện đại trên nền tảng AWS, tập trung vào các lĩnh vực quan trọng như bảo mật hệ thống, container hóa, cơ sở dữ liệu thế hệ mới và kiến trúc ứng dụng thời gian thực.
- Tìm hiểu cách kết hợp giữa Machine Learning, Generative AI và các dịch vụ AWS để xây dựng những hệ thống thông minh, có khả năng xử lý dữ liệu phức tạp và hỗ trợ ra quyết định trong thực tế.
- Tiếp cận các mô hình kiến trúc Cloud hiện đại như GraphRAG, Serverless Architecture và Real-time Application nhằm hiểu rõ hơn cách doanh nghiệp triển khai các hệ thống có khả năng mở rộng cao.
- Học hỏi kinh nghiệm thực tế từ các chuyên gia trong ngành về lộ trình phát triển nghề nghiệp, từ các vị trí nền tảng như IT Helpdesk, System Administrator đến các vai trò chuyên sâu như Cloud Engineer, DevOps Engineer.
- Nâng cao nhận thức về tầm quan trọng của kỹ năng mềm, khả năng làm việc nhóm, giao tiếp và tinh thần học tập liên tục trong môi trường công nghệ thay đổi nhanh chóng.

### Thông Tin Sự Kiện

- **Tên sự kiện:** AWS Community Meetup.
- **Chuỗi chương trình:** First Cloud Journey.
- **Thời gian:** Ngày 06/06/2026.
- **Hình thức:** Hội thảo công nghệ (Technical Community Event).
- **Đối tượng tham gia:** Sinh viên, kỹ sư phần mềm, Cloud Engineer, DevOps Engineer, AI Engineer và cộng đồng yêu thích công nghệ AWS.
- **Chủ đề chính:** Cloud Computing, Machine Learning, Generative AI, Containerization, Graph Database, Real-time Architecture và DevOps.

### Danh Sách Diễn Giả

- **Trương Huy Phước** - Diễn giả chuyên đề về nghệ thuật làm việc nhóm hiệu quả.
- **Việt Phát** - Sinh viên chuyên ngành AI tại Swinburne University of Technology.
- **Trần Trung Vinh** - Senior System Administrator tại Central Retail Group.
- **Bảo Huỳnh** - Junior Cloud Native Developer tại Endava Vietnam, Founder ITea Lab.
- **Nguyễn Quốc Bảo** - Diễn giả chuyên đề về kiến trúc Game Multiplayer trên Cloud.
- **Lê Hoàng Gia Đại** - Sinh viên năm cuối Đại học HUTECH, thành viên AWS G3 Team.

### Nội Dung Nổi Bật

Sự kiện AWS Community Meetup tập trung vào nhiều chủ đề quan trọng trong hệ sinh thái Cloud hiện đại, từ xây dựng hạ tầng bảo mật, triển khai ứng dụng container hóa, phát triển hệ thống AI thế hệ mới cho đến kiến trúc ứng dụng thời gian thực.

Thay vì chỉ giới thiệu các dịch vụ AWS riêng lẻ, các diễn giả tập trung phân tích cách kết hợp nhiều công nghệ khác nhau để giải quyết những bài toán thực tế trong doanh nghiệp. Các nội dung được trình bày không chỉ mang tính lý thuyết mà còn đi kèm với các ví dụ triển khai, kinh nghiệm vận hành hệ thống và những bài học thực tế trong quá trình phát triển sản phẩm.


#### Kết hợp Machine Learning với AWS WAF trong bảo mật hệ thống

Một trong những chủ đề nổi bật của sự kiện là việc ứng dụng Machine Learning để nâng cao khả năng bảo mật cho các hệ thống Web trên AWS.

Theo cách tiếp cận truyền thống, AWS WAF thường hoạt động dựa trên các bộ luật định sẵn (Rule-based / Signature-based), giúp phát hiện và ngăn chặn các dạng tấn công phổ biến như SQL Injection, Cross-site Scripting (XSS) hoặc các hành vi truy cập bất thường đã được xác định trước.

Tuy nhiên, phương pháp này gặp hạn chế khi phải đối mặt với những cuộc tấn công mới hoặc các mối đe dọa chưa từng xuất hiện trước đó (Zero-day Attack). Do không có thông tin nhận diện sẵn, các hệ thống bảo mật truyền thống có thể gặp khó khăn trong việc phát hiện các hành vi bất thường.

Giải pháp được chia sẻ trong sự kiện là kết hợp Machine Learning với hệ thống bảo mật AWS để xây dựng cơ chế phát hiện thông minh hơn.

Một số nội dung nổi bật:
- Sử dụng mô hình Machine Learning như LightGBM để phân tích hành vi truy cập và nhận diện các mẫu bất thường.
- Kết hợp nhiều dịch vụ AWS như VPC, EC2, Application Load Balancer, AWS WAF, Security Hub, GuardDuty và Amazon Kinesis để xây dựng hệ thống giám sát bảo mật theo thời gian thực.
- Chuyển đổi từ mô hình bảo mật phản ứng (Reactive Security) sang mô hình chủ động phát hiện và ngăn chặn nguy cơ.
Qua phần trình bày này, tôi nhận thấy bảo mật Cloud hiện đại không còn chỉ dựa vào các luật cố định mà cần kết hợp giữa tự động hóa, phân tích dữ liệu và trí tuệ nhân tạo để có khả năng thích ứng với những mối đe dọa mới.

#### Docker và công nghệ Containerization

Một nội dung quan trọng khác trong sự kiện là công nghệ container hóa với Docker, một trong những nền tảng phổ biến trong quá trình phát triển và triển khai phần mềm hiện nay.

Trước khi có container, doanh nghiệp thường sử dụng máy ảo (Virtual Machine) để đóng gói ứng dụng. Tuy nhiên, mỗi máy ảo cần một hệ điều hành riêng, dẫn đến việc tiêu tốn nhiều tài nguyên và làm tăng thời gian triển khai.

Docker giải quyết vấn đề này bằng cách đóng gói ứng dụng cùng toàn bộ thư viện phụ thuộc vào một container nhỏ gọn, có thể chạy nhất quán trên nhiều môi trường khác nhau.

Một số điểm nổi bật:

- Loại bỏ vấn đề "Code chạy được trên máy tôi nhưng không chạy trên môi trường khác".
- Đóng gói ứng dụng, thư viện và cấu hình thành Docker Image có thể tái sử dụng.
- Hỗ trợ triển khai nhanh chóng trong các hệ thống CI/CD.
- Là nền tảng quan trọng cho kiến trúc Microservices và Cloud Native Application.

Thông qua nội dung này, tôi hiểu rõ hơn vai trò của Docker trong quá trình hiện đại hóa quy trình phát triển phần mềm, đặc biệt khi kết hợp với các dịch vụ Cloud có khả năng mở rộng tự động.


#### Xây dựng hệ thống Multiplayer Real-time trên AWS

Một chủ đề thú vị khác là kiến trúc xây dựng trò chơi Multiplayer trên nền tảng Cloud.

Phần trình bày giới thiệu cách kết hợp giữa Game Engine Godot và các dịch vụ AWS để xây dựng hệ thống có khả năng giao tiếp thời gian thực giữa nhiều người chơi.

Kiến trúc được đề cập bao gồm:

- Client game được phát triển bằng Godot Engine.
- AWS API Gateway sử dụng WebSocket để duy trì kết nối hai chiều giữa Client và Server.
- AWS Lambda xử lý logic backend theo mô hình Serverless.
- Amazon DynamoDB lưu trữ trạng thái người chơi và dữ liệu phiên chơi.

Một số vấn đề thực tế cũng được phân tích như:

- Xử lý tình trạng mất kết nối WebSocket (GoneException).
- Tối ưu chi phí khi số lượng người chơi tăng cao.
- Lựa chọn kiến trúc phù hợp giữa Serverless Architecture và Dedicated Game Server.

Qua phần chia sẻ này, tôi hiểu rõ hơn cách thiết kế các hệ thống yêu cầu độ trễ thấp và khả năng đồng bộ dữ liệu liên tục, không chỉ trong lĩnh vực game mà còn trong nhiều ứng dụng real-time khác như chat, cộng tác trực tuyến hoặc IoT.

#### Amazon Neptune và GraphRAG trong ứng dụng Generative AI

Một trong những chủ đề mang tính xu hướng của sự kiện là việc kết hợp giữa **Generative AI**, **Large Language Models (LLMs)** và cơ sở dữ liệu đồ thị (**Graph Database**) để nâng cao khả năng suy luận của hệ thống AI.

Trước đây, các ứng dụng sử dụng mô hình **Retrieval-Augmented Generation (RAG)** thường dựa chủ yếu vào việc tìm kiếm các đoạn văn bản có liên quan trong kho dữ liệu rồi cung cấp cho mô hình ngôn ngữ để tạo câu trả lời.

Tuy nhiên, với những bài toán phức tạp yêu cầu hiểu mối quan hệ giữa nhiều thực thể khác nhau, phương pháp RAG truyền thống có thể gặp hạn chế trong việc suy luận nhiều bước.

Giải pháp được giới thiệu trong sự kiện là **GraphRAG**, một phương pháp mở rộng RAG bằng cách kết hợp mô hình ngôn ngữ với cơ sở dữ liệu đồ thị.

Một số nội dung nổi bật:

- Sử dụng **Amazon Neptune** làm nền tảng lưu trữ Knowledge Graph, giúp biểu diễn các mối quan hệ phức tạp giữa dữ liệu.
- Kết hợp với **Amazon Bedrock** để khai thác sức mạnh của các mô hình Generative AI trong quá trình phân tích và tạo phản hồi.
- Hỗ trợ khả năng suy luận nhiều bước (**Multi-hop Reasoning**) thông qua việc truy vấn các mối quan hệ trong đồ thị thay vì chỉ tìm kiếm từ khóa.
- Có thể triển khai theo nhiều hướng khác nhau:
  - Sử dụng **Amazon Bedrock Knowledge Bases kết hợp Neptune Analytics** để đơn giản hóa quá trình triển khai.
  - Sử dụng các framework như **LlamaIndex** để tùy chỉnh quy trình xử lý dữ liệu và truy vấn.

Thông qua nội dung này, tôi nhận thấy rằng trong các hệ thống AI doanh nghiệp, việc quản lý dữ liệu và xây dựng ngữ cảnh đóng vai trò quan trọng không kém việc lựa chọn mô hình AI. Một mô hình mạnh nhưng thiếu dữ liệu phù hợp vẫn khó có thể đưa ra kết quả chính xác.


#### Hành trình phát triển nghề nghiệp từ IT Helpdesk đến Cloud Engineer

Bên cạnh các chủ đề kỹ thuật, sự kiện cũng mang đến một góc nhìn thực tế về quá trình phát triển nghề nghiệp trong lĩnh vực công nghệ thông tin.

Thông qua câu chuyện chuyển đổi từ vị trí **IT Helpdesk** đến **Senior System Administrator** và định hướng trở thành **Cloud/DevOps Engineer**, diễn giả chia sẻ rằng việc phát triển sự nghiệp không chỉ dựa vào chứng chỉ mà cần tập trung vào năng lực thực tế và khả năng giải quyết vấn đề.

Một số bài học quan trọng được chia sẻ:

- Thay đổi tư duy từ quản lý máy chủ truyền thống sang tư duy quản lý hạ tầng Cloud theo mô hình **Pay-as-you-go**.
- Làm quen với các công cụ hiện đại như:
  - Infrastructure as Code (Terraform).
  - Continuous Integration / Continuous Deployment (CI/CD).
  - Monitoring và Automation.
- Tự động hóa các công việc lặp lại thay vì xử lý thủ công.
- Luôn kiểm tra kỹ trước khi thay đổi hệ thống Production.
- Xây dựng các dự án cá nhân và Portfolio thực tế thay vì chỉ tập trung vào việc đạt chứng chỉ.

Phần chia sẻ này giúp tôi hiểu rằng con đường phát triển trong ngành Cloud không nhất thiết phải bắt đầu từ một vị trí cụ thể, mà quan trọng hơn là khả năng học hỏi liên tục, tích lũy kinh nghiệm thực tế và chủ động mở rộng kiến thức.


#### Nghệ thuật làm việc nhóm hiệu quả trong môi trường công nghệ

Ngoài các nội dung kỹ thuật, sự kiện cũng dành một phần quan trọng để chia sẻ về kỹ năng làm việc nhóm – một yếu tố ảnh hưởng trực tiếp đến sự thành công của các dự án công nghệ.

Diễn giả nhấn mạnh rằng một đội nhóm hiệu quả không chỉ cần những cá nhân có năng lực chuyên môn mà còn cần khả năng phối hợp, giao tiếp và chia sẻ trách nhiệm.

Bốn nguyên tắc quan trọng được đề cập gồm:

##### Xác định mục tiêu chung
Các thành viên cần hiểu rõ mục tiêu cuối cùng của dự án để có thể phối hợp và đưa ra quyết định thống nhất.

##### Phân công đúng người, đúng việc
Mỗi thành viên nên đảm nhận những nhiệm vụ phù hợp với điểm mạnh của bản thân nhằm tối ưu hiệu quả làm việc.

##### Giao tiếp cởi mở
Việc trao đổi thường xuyên, chủ động lắng nghe và chia sẻ khó khăn giúp giảm thiểu sai lệch trong quá trình phát triển.

##### Đề cao trách nhiệm cá nhân
Mỗi thành viên cần chịu trách nhiệm với phần việc của mình thay vì phụ thuộc hoàn toàn vào các thành viên khác.

Bên cạnh đó, diễn giả cũng giới thiệu một số công cụ hỗ trợ làm việc nhóm như:

- Trello.
- ClickUp.
- Google Workspace.
- Slack.
- Discord.

Qua phần trình bày này, tôi nhận thấy rằng kỹ năng mềm là yếu tố không thể thiếu đối với kỹ sư phần mềm, đặc biệt trong các dự án Cloud và AI có tính phức tạp cao.


### Những Gì Học Được

#### Tư duy thiết kế hệ thống hiện đại

Thông qua các bài chia sẻ tại sự kiện, tôi nhận thấy việc xây dựng một hệ thống công nghệ hiện đại không chỉ tập trung vào việc lựa chọn công nghệ mới mà cần xem xét tổng thể về khả năng mở rộng, bảo mật, chi phí và khả năng vận hành lâu dài.

Một số bài học quan trọng:

- Hiểu được vai trò của mô hình **Container-First** trong việc xây dựng ứng dụng Cloud Native, giúp hệ thống dễ triển khai, mở rộng và duy trì trên nhiều môi trường khác nhau.
- Nhận thức được tầm quan trọng của việc lựa chọn đúng mô hình dữ liệu. Với những bài toán yêu cầu phân tích mối quan hệ phức tạp, Graph Database có thể mang lại nhiều lợi thế hơn so với cơ sở dữ liệu quan hệ truyền thống.
- Hiểu rằng kiến trúc hệ thống cần được thiết kế dựa trên yêu cầu thực tế thay vì chỉ lựa chọn công nghệ theo xu hướng.

#### Kiến trúc Cloud và bảo mật hệ thống

Sự kiện giúp tôi hiểu rõ hơn cách xây dựng các hệ thống Cloud có tính bảo mật và khả năng mở rộng cao.

Các kiến thức quan trọng bao gồm:

- Hiểu cách kết hợp Machine Learning với AWS WAF để xây dựng hệ thống bảo mật thông minh, có khả năng phát hiện các hành vi bất thường thay vì chỉ dựa vào các luật cố định.
- Nắm được cách triển khai các ứng dụng thời gian thực bằng WebSocket, Lambda và DynamoDB.
- Hiểu vai trò của Docker trong việc chuẩn hóa môi trường triển khai và hỗ trợ quy trình CI/CD.
- Nhận thức được tầm quan trọng của việc áp dụng các nguyên tắc Security by Design ngay từ giai đoạn thiết kế hệ thống.


#### Generative AI và quản lý dữ liệu

Một trong những kiến thức quan trọng nhất tôi tiếp nhận được là vai trò của dữ liệu trong các hệ thống AI.

Các bài học nổi bật:

- Hiểu rằng chất lượng của hệ thống AI không chỉ phụ thuộc vào mô hình ngôn ngữ mà còn phụ thuộc vào cách tổ chức dữ liệu và xây dựng ngữ cảnh.
- Hiểu được sự khác biệt giữa RAG truyền thống và GraphRAG trong việc xử lý các bài toán cần suy luận nhiều bước.
- Nhận thức được tiềm năng của Amazon Bedrock và các dịch vụ AI trên AWS trong việc xây dựng ứng dụng thông minh.


#### Kỹ năng nghề nghiệp và làm việc nhóm

Bên cạnh kiến thức kỹ thuật, sự kiện cũng giúp tôi nhận ra vai trò quan trọng của kỹ năng mềm trong quá trình phát triển sự nghiệp.

Một số bài học:

- Không ngừng học hỏi và cập nhật công nghệ mới.
- Chủ động xây dựng các dự án thực tế để nâng cao kinh nghiệm.
- Kết hợp kỹ năng chuyên môn với khả năng giao tiếp và làm việc nhóm.
- Hiểu rằng một kỹ sư công nghệ giỏi không chỉ giải quyết vấn đề kỹ thuật mà còn cần hiểu nhu cầu của người dùng và doanh nghiệp.

### Ứng Dụng Vào Công Việc & Đồ Án

Những kiến thức tiếp thu được từ AWS Community Meetup có thể được áp dụng trực tiếp vào quá trình phát triển dự án cũng như định hướng nghề nghiệp trong tương lai.

- **Tăng cường bảo mật Backend:**  
Áp dụng các kiến thức về AWS WAF, Machine Learning và kiến trúc bảo mật Cloud để xây dựng lớp bảo vệ tốt hơn cho hệ thống Backend của Website Đặt Sân Bóng Đá. Các phương pháp phát hiện hành vi bất thường có thể được nghiên cứu nhằm nâng cao khả năng kiểm soát lưu lượng truy cập và giảm thiểu các nguy cơ tấn công vào hệ thống.
- **Triển khai Container hóa ứng dụng:**  
Sử dụng Docker để đóng gói Backend Java Spring Boot, giúp chuẩn hóa môi trường phát triển và triển khai. Việc áp dụng Container giúp giảm sự khác biệt giữa môi trường Local, Testing và Production, đồng thời tạo nền tảng thuận lợi khi triển khai trên AWS với các mô hình như ECS hoặc Kubernetes trong tương lai.
- **Cải thiện khả năng ứng dụng AI:**  
Nghiên cứu áp dụng kiến trúc GraphRAG kết hợp với Amazon Bedrock và Knowledge Base để phát triển các tính năng AI thông minh hơn. Thay vì chỉ tìm kiếm thông tin dựa trên từ khóa, hệ thống có thể khai thác mối quan hệ giữa dữ liệu để đưa ra câu trả lời có ngữ cảnh và độ chính xác cao hơn.
- **Áp dụng kiến trúc Real-time khi cần thiết:**  
Những kiến thức về WebSocket và mô hình Serverless giúp tôi có thêm góc nhìn trong việc xây dựng các tính năng cần cập nhật dữ liệu theo thời gian thực như thông báo, trạng thái đặt sân hoặc tương tác trực tiếp giữa người dùng.
- **Phát triển kỹ năng làm việc nhóm:**  
Các nguyên tắc về giao tiếp, phân chia nhiệm vụ và quản lý tiến độ được chia sẻ trong sự kiện có thể áp dụng vào quá trình thực hiện đồ án nhóm, giúp cải thiện hiệu quả phối hợp giữa các thành viên.


### Trải Nghiệm Trong Sự Kiện

Tham gia AWS Community Meetup ngày 06/06/2026 là một trải nghiệm có giá trị trong quá trình học tập và định hướng phát triển trong lĩnh vực Cloud Computing.

#### Tiếp cận kiến thức thực tế từ các chuyên gia trong ngành:
Được lắng nghe những chia sẻ trực tiếp từ các kỹ sư, Cloud Developer và những người đang làm việc trong lĩnh vực AWS giúp tôi hiểu rõ hơn khoảng cách giữa kiến thức lý thuyết và yêu cầu thực tế của doanh nghiệp.

#### Mở rộng góc nhìn về kiến trúc hệ thống hiện đại: 
Các bài trình bày về AWS WAF, Docker, WebSocket, Amazon Neptune và GraphRAG giúp tôi hiểu rằng việc xây dựng một hệ thống hoàn chỉnh không chỉ cần lựa chọn công nghệ phù hợp mà còn phải cân nhắc về bảo mật, khả năng mở rộng và chi phí vận hành.

####  Hiểu rõ hơn về xu hướng phát triển của ngành công nghệ:  
Thông qua các chủ đề về Generative AI, Machine Learning Security và Cloud Native Architecture, tôi nhận thấy AI và Cloud đang ngày càng được kết hợp chặt chẽ để tạo ra những giải pháp thông minh và tự động hóa hơn.

#### Có thêm định hướng phát triển nghề nghiệp:
Những chia sẻ về hành trình từ IT Helpdesk đến Cloud Engineer/DevOps Engineer giúp tôi hiểu rõ hơn về lộ trình phát triển kỹ năng, tầm quan trọng của việc xây dựng nền tảng vững chắc và tích lũy kinh nghiệm thực tế.

#### Kết nối với cộng đồng công nghệ:
Sự kiện cũng là cơ hội để trao đổi, học hỏi từ những người có cùng định hướng, từ đó mở rộng kiến thức và tạo động lực tiếp tục phát triển bản thân trong lĩnh vực công nghệ.


### Bài Học Rút Ra

Qua sự kiện AWS Community Meetup, tôi nhận thấy rằng việc trở thành một kỹ sư phần mềm hiện đại không chỉ yêu cầu khả năng lập trình mà còn cần hiểu biết về kiến trúc hệ thống, bảo mật và cách vận hành ứng dụng trên môi trường Cloud.

Một số bài học quan trọng:

- **Cloud Security cần được thiết kế ngay từ đầu:**  
Bảo mật không nên chỉ được bổ sung sau khi hệ thống hoàn thành mà cần được xem xét ngay trong quá trình thiết kế kiến trúc. Việc kết hợp các công cụ như AWS WAF, Security Hub và các phương pháp phân tích dữ liệu giúp hệ thống có khả năng phòng vệ chủ động hơn.
- **Nắm vững các công nghệ nền tảng là yếu tố quan trọng:**  
Docker, Database Architecture, WebSocket và các dịch vụ AWS là những kiến thức nền tảng giúp kỹ sư có khả năng xây dựng các hệ thống hiện đại, dễ mở rộng và phù hợp với môi trường doanh nghiệp.
- **AI trong thực tế cần kết hợp giữa mô hình, dữ liệu và kiến trúc:**  
Một hệ thống AI hiệu quả không chỉ phụ thuộc vào mô hình ngôn ngữ mạnh mà còn cần dữ liệu chất lượng, cách tổ chức thông tin hợp lý và cơ chế kiểm soát đầu ra.
- **Kỹ năng mềm đóng vai trò quan trọng trong môi trường công nghệ:**  
Khả năng giao tiếp, làm việc nhóm, chia sẻ kiến thức và tinh thần tự học liên tục là những yếu tố cần thiết để phát triển lâu dài trong ngành IT.
- **Luôn duy trì tư duy học hỏi và cập nhật công nghệ:**  
Lĩnh vực Cloud và AI thay đổi rất nhanh, vì vậy việc liên tục nghiên cứu, thực hành và xây dựng các dự án thực tế là yếu tố quan trọng để nâng cao năng lực cá nhân.

---

### Một Số Hình Ảnh Khi Tham Gia Sự Kiện

![Hình ảnh tham gia sự kiện 2](/images/4-Event/Event2-1.jpg)
![Hình ảnh tham gia sự kiện 2](/images/4-Event/Event2-2.png)