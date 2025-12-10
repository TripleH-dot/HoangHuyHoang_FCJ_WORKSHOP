---
title: "Event 2"
date: "2025-11-17"
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---



# Bài thu hoạch “AWS Cloud Mastery Series #2”

### Mục Đích Của Sự Kiện

- Giới thiệu tư duy DevOps, văn hoá và các chỉ số quan trọng
- Trình bày các dịch vụ DevOps của AWS để xây dựng pipeline CI/CD hoàn chỉnh
- Minh hoạ Infrastructure as Code với CloudFormation và AWS CDK
- Khám phá dịch vụ container và các chiến lược triển khai hiện đại
- Thực hành trực tiếp với công cụ giám sát và quan sát hệ thống
- Chia sẻ best practices và các case study thực tế về DevOps

### Danh Sách Diễn Giả

Các diễn giả đã làm việc tại aws hoặc các đối tác của aws

### Nội Dung Nổi Bật

#### Phần mở đầu & Tư duy DevOps

- Tổng kết lại buổi AI/ML trước đó và cách DevOps giúp tăng tốc quy trình ML
- Các nguyên tắc cốt lõi của DevOps: cộng tác, tự động hóa, đo lường, cải tiến liên tục
- Các chỉ số hiệu suất: DORA metrics, MTTR, tần suất triển khai

#### Dịch vụ AWS DevOps – Xây dựng CI/CD Pipeline

- **Quản lý mã nguồn**: CodeCommit, GitFlow vs Trunk-based
- **Build & Test**: cấu hình CodeBuild, tích hợp kiểm thử tự động
- **Chiến lược triển khai**: Blue/Green, Canary, Rolling deployments
- **CodePipeline**: điều phối end-to-end với tự động hóa đa tầng
Demo trực tiếp: thực thi pipeline CI/CD hoàn chỉnh

#### Infrastructure as Code (IaC)

- **AWS CloudFormation**: template, stack, drift detection
- **AWS CDK**: construct, pattern tái sử dụng, hỗ trợ đa ngôn ngữ
- **Demo**: triển khai tài nguyên bằng CloudFormation và CDK
- **So sánh**: khi nào dùng CloudFormation và khi nào nên chọn CDK

#### Dịch vụ Container trên AWS

- Kiến thức Docker cơ bản và kiến trúc microservices
- Amazon ECR: lưu trữ image, quét bảo mật, lifecycle policy
- **ECS vs EKS**: chiến lược triển khai, scaling, orchestration
- AWS App Runner: triển khai container đơn giản cho developer
- Case study & demo: so sánh quy trình triển khai giữa các dịch vụ

#### Monitoring & Observability

- CloudWatch: metrics, logs, dashboards, alarms
- AWS X-Ray: tracing phân tán và phân tích độ trễ
- Demo: thiết lập quan sát toàn bộ hệ thống từ ứng dụng đến hạ tầng
- Best practices cho cảnh báo, dashboard và quy trình trực on-call

#### DevOps Best Practices & Case Studies

- Các kỹ thuật triển khai: feature flags, A/B testing
- Kiểm thử tự động tích hợp vào CI/CD
- Quy trình xử lý sự cố và postmortem
- Case study: doanh nghiệp nhỏ đến doanh nghiệp lớn triển khai DevOps như thế nào

### Những Gì Học Được

#### Tư Duy DevOps

- Cộng tác + tự động hóa = triển khai nhanh hơn, an toàn hơn
- Cải tiến liên tục dựa trên các chỉ số khách quan (DORA)
- Áp dụng “shift-left” cho kiểm thử, bảo mật và giám sát

#### Kiến Trúc Kỹ Thuật

- Xây dựng pipeline CI/CD tự động với CodePipeline
- Dùng IaC (CloudFormation/CDK) để tạo môi trường nhất quán, dễ lặp lại
- Triển khai container với ECS/EKS tùy theo workload
- Thiết lập observability mạnh mẽ bằng CloudWatch + X-Ray

#### Chiến Lược DevOps

- Tiến tới triển khai tự động và workflow dựa trên Git
- Xây dựng tiêu chuẩn giám sát và ngưỡng cảnh báo
- Tích hợp feature flags và chiến lược triển khai từng phần
- Tạo văn hoá học hỏi qua postmortem và retrospectives

### Ứng Dụng Vào Công Việc

- Triển khai CI/CD cho các dự án hiện tại và tương lai
- Chuẩn hoá việc tạo hạ tầng bằng IaC
- Ứng dụng container và đánh giá ECS/EKS cho microservices
- Cải thiện quan sát hệ thống bằng dashboard, cảnh báo, tracing
- Tích hợp kiểm thử tự động vào pipeline
- Giảm rủi ro bằng các chiến lược triển khai (blue/green, canary)

### Trải nghiệm trong event

Tham gia workshop “DevOps on AWS” giúp tôi có góc nhìn rõ ràng và hệ thống hơn về cách xây dựng workflow DevOps hiện đại với các dịch vụ AWS.

#### Học hỏi từ các diễn giả có chuyên môn cao
- Hiểu cách văn hoá DevOps tăng tốc độ và chất lượng phát triển
- Nắm vững giải pháp AWS-native cho CI/CD, IaC, container

#### Trải nghiệm thực hành

- Tự tay xây dựng pipeline với CodePipeline
- Viết IaC bằng CloudFormation và CDK
- Thiết lập quan sát cho ứng dụng phân tán

#### Bài học thực tế & thảo luận

- Hiểu cách doanh nghiệp triển khai DevOps ở nhiều quy mô
- Nắm được vai trò của tự động hóa và giám sát trong vận hành hiệu quả


#### Một số hình ảnh khi tham gia sự kiện
![Event2](/images/4-EventParticipated/4.2-Event2/event2.jpg)  
> Nhìn chung, sự kiện giúp tôi củng cố kiến thức DevOps trên AWS và định hình lại cách tiếp cận trong tự động hóa, quy trình triển khai và tối ưu vận hành.
