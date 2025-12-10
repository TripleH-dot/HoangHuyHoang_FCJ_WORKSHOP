---
title: "Event 3"
date: "2025-11-29"
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch “AWS Cloud Mastery Series #3”

### Mục Đích Của Sự Kiện

- Hiểu vai trò của **Security Pillar** trong AWS Well-Architected Framework
- Nắm các nguyên tắc cốt lõi: **Least Privilege, Zero Trust, Defense in Depth**
- Cập nhật mô hình **Shared Responsibility** và các mối đe doạ phổ biến tại Việt Nam
- Tìm hiểu kiến trúc IAM hiện đại, giám sát liên tục, bảo vệ hạ tầng, bảo vệ dữ liệu
- Thực hành xây dựng **Incident Response Playbooks** và tự động hóa phản ứng

### Danh Sách Diễn Giả

Các diễn giả đã làm việc tại aws hoặc các đối tác của aws

### Nội Dung Nổi Bật

#### Mở đầu - Nền tảng bảo mật

- Vai trò của **Security Pillar** trong AWS Well-Architected
- Các nguyên tắc cốt lõi: Least Privilege, Zero Trust, Defense in Depth
- **Shared Responsibility Model** trong môi trường cloud
- Các mối đe dọa đám mây phổ biến với doanh nghiệp tại Việt Nam

#### Identity & Access Management – Kiến trúc IAM hiện đại

- IAM Users, Roles, Policies → tránh **long-term credentials**
- IAM Identity Center: **SSO, permission sets**
- SCP và permission boundaries cho mô hình **multi-account**
- MFA, xoay vòng thông tin xác thực, Access Analyzer
- Mini-demo: xác thực policy + mô phỏng quyền truy cập

#### Detection – Giám sát và phát hiện liên tục

- CloudTrail (tầm tổ chức), GuardDuty, Security Hub
- Logging đa tầng: **VPC Flow Logs, ALB logs, S3 access logs**
- Cảnh báo & tự động hóa bằng **EventBridge**
- Giới thiệu **Detection-as-Code**: hạ tầng + luật phát hiện

#### Infrastructure Protection – Bảo mật hạ tầng và workload

- Phân tầng VPC, phân tách public/private
- Security Groups vs NACLs: cách dùng đúng
- WAF + Shield + Network Firewall
- Các nguyên tắc bảo mật cho **EC2, ECS, EKS**

#### Data Protection – Mã hóa, Key & Secrets

- KMS: key policies, grants, key rotation
- Mã hóa khi lưu trữ & truyền tải cho **S3, EBS, RDS, DynamoDB**
- Secrets Manager & Parameter Store: mô hình xoay vòng
- Phân loại dữ liệu và thiết lập guardrails

#### Incident Response – Playbook & Tự động hóa

- Vòng đời xử lý sự cố trong AWS
- Ví dụ playbook: rò rỉ IAM key, S3 bị public, EC2 bị malware
- Snapshot, cô lập, thu thập bằng chứng
- Tự động phản hồi bằng **Lambda / Step Functions**

### Những Gì Học Được

#### Tư Duy Thiết Kế

- **Least privilege** làm mặc định
- **Zero Trust**: luôn xác minh, không giả định tin cậy
- **Defense in Depth**: bảo vệ đa lớp từ identity → network → workload → data
- Áp dụng baseline bảo mật **multi-account** theo best practice của AWS

#### Kiến Trúc Kỹ Thuật

- IAM hiện đại: Identity Center + permission boundaries
- Logging đa tầng & tư duy Detection-as-Code
- Bảo vệ hạ tầng: VPC, SG/NACL, WAF, Firewall
- Bảo vệ dữ liệu toàn diện: mã hóa, vòng đời khóa, xoay vòng secret
- Tự động hóa xử lý sự cố để giảm thời gian phản hồi

#### Chiến lược bảo mật đám mây

- Tập trung vào **visibility + prevention + response**
- Chuẩn hóa môi trường multi-account theo best practice
- Ưu tiên **giám sát liên tục**
- Tăng cường tự động hóa để vận hành nhanh và ổn định hơn
- Đánh giá posture thường xuyên bằng GuardDuty + Security Hub

### Ứng Dụng Vào Công Việc

- Chuẩn hóa IAM: loại bỏ long-term keys, bắt buộc MFA, xoay vòng thông tin
- Kích hoạt logging đa tầng với guardrails phù hợp
- Rà soát & tối ưu phân đoạn VPC
- Bắt buộc mã hóa dữ liệu ở mọi dịch vụ lưu trữ
- Xây dựng IR playbooks cho từng loại sự cố
- Tự động hóa phản hồi using EventBridge + Lambda

### Trải nghiệm trong event

Sự kiện mang đến cái nhìn toàn diện và hệ thống về cách thiết kế bảo mật theo chuẩn AWS Well-Architected.

#### Học hỏi từ các diễn giả có chuyên môn cao

- Hiểu rõ cách AWS định nghĩa & triển khai **Security Pillar**
- Nắm được IAM hiện đại và mô hình multi-account
- Hiểu cách doanh nghiệp Việt Nam đối mặt và giảm thiểu rủi ro cloud

#### Trải nghiệm kỹ thuật thực hành

- Thực hành xác thực IAM policies
- Xây dựng detection & quy trình cảnh báo tự động
- Thiết kế và vận hành Incident Response Playbooks

#### Hiểu về security orchestration

- Hiểu cách tích hợp GuardDuty, CloudTrail, Security Hub
- Nắm cách áp dụng Detection-as-Code thực tế

#### Kết nối & trao đổi

- Chia sẻ kiến thức với chuyên gia cloud security
- Học kinh nghiệm thực tế từ các doanh nghiệp lớn

#### Bài học rút ra

- Bảo mật cloud cần tiếp cận chủ động, đa lớp
- Identity là lớp phòng thủ quan trọng nhất
- Logging, quan sát và tự động hóa phải được ưu tiên
- IR playbooks và auto-response là điều bắt buộc

#### Một số hình ảnh khi tham gia sự kiện
![Event3](/images/4-EventParticipated/4.3-Event3/event3.jpg) 

> Tổng thể, sự kiện không chỉ củng cố nền tảng bảo mật đám mây của tôi mà còn giúp tôi định hình lại tư duy trong thiết kế kiến trúc an toàn, áp dụng các best practice hiện đại của AWS và cải thiện kỹ năng vận hành giữa các nhóm.
