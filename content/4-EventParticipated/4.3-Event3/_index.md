---
title: "Event 3"
date: "2025-11-29"
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---



# Summary Report: “AWS Cloud Mastery Series #3”

### Event Objectives

- Understand the role of the Security Pillar in the AWS Well-Architected Framework
- Learn the core principles: Least Privilege, Zero Trust, Defense in Depth
- Review the Shared Responsibility Model and common cloud threats in Vietnam
- Explore modern IAM architecture, continuous monitoring, infrastructure and data protection
- Practice building Incident Response Playbooks and security automation

### Speakers

Speakers have worked at AWS or AWS partners.

### Key Highlights

#### Opening – Security Foundation

- Role of the **Security Pillar** in AWS Well-Architected
- Core principles: Least Privilege, Zero Trust, Defense in Depth
- **Shared Responsibility Model** in cloud environments
- Top cloud threats commonly faced by businesses in Vietnam

#### Identity & Access Management: Modern IAM Architecture

- IAM Users, Roles, Policies → avoid **long-term credentials**
- IAM Identity Center: **SSO, permission sets**
- SCP & permission boundaries for **multi-account** governance
- MFA, credential rotation, Access Analyzer
- Mini-demo: Policy validation + access simulation 

#### Detection: Detection & Continuous Monitoring

- CloudTrail (organization-level), GuardDuty, Security Hub
- Multi-layer logging: **VPC Flow Logs, ALB logs, S3 access logs**
- Alerting & automation using **EventBridge**
- Introduction to **Detection-as-Code**: infrastructure + rules 

#### Infrastructure Protection: Network & Workload Security

- VPC segmentation, public vs private placement
- Security Groups vs NACLs: correct usage patterns
- WAF + Shield + Network Firewall
- Workload protection essentials: **EC2, ECS, EKS**

#### Data Protection: Encryption, Keys & Secrets

- KMS: key policies, grants, key rotation

Encryption at-rest & in-transit for **S3, EBS, RDS, DynamoDB**

Secrets Manager & Parameter Store: rotation patterns

Data classification & access guardrails 

#### Incident Response: IR Playbook & Automation

- AWS Incident Response lifecycle
- Example playbooks: compromised IAM key, S3 public exposure, EC2 malware detection
- Snapshot, isolation, evidence collection
- Automated response via **Lambda / Step Functions**

### Key Takeaways

#### Security Design Mindset

- **Least privilege as default**: grant only what’s necessary
- **Zero Trust**: verify every access, never assume trust
- **Defense in Depth**: layered protection across identity, network, workload, and data
- Adopt a **multi-accoun**t security baseline aligned with AWS best practices

#### Technical Architecture

- Modern IAM architecture: Identity Center + permission boundaries
- Comprehensive multi-layer logging and Detection-as-Code mindset
- Infrastructure protection across VPC, SG/NACL, WAF, Firewall
- Full-spectrum data protection: encryption, key lifecycle, secret rotation
- Automating incident response to reduce reaction time

#### Cloud Security Strategy

- Focus on **visibility + prevention + response**
- Standardize multi-account environments using AWS best practices
- Emphasize **continuous monitoring**
- Increase automation for faster and more reliable security operations
- Regularly evaluate security posture with GuardDuty + Security Hub 

### Applying to Work

- Standardize IAM: remove long-term keys, enforce MFA, apply rotation
- Enable complete multi-layer logging with proper guardrails
- Review and optimize VPC segmentation
- Enforce encryption across all data storage services
- Build IR playbooks tailored to each type of incident
- Automate responses using EventBridge + Lambda

### Event Experience

Attending the event provided a structured and comprehensive understanding of how to design security following AWS Well-Architected best practices.

#### Learning from highly skilled speakers
- Gained a clear view of how AWS defines and implements the **Security Pillar**
- Learned modern IAM architecture and common multi-account patterns
- Understood how Vietnamese businesses face and mitigate cloud threats 

#### Hands-on technical exposure
- Practiced validating IAM policies
- Experienced building detection & automated alerting workflows
- Learned how to design and operate Incident Response Playbooks  

#### Understanding security orchestration
- Understood the integration of GuardDuty, CloudTrail, and Security Hub
- Learned how to approach Detection-as-Code in real environments 

#### Networking and discussions
- Exchanged insights with cloud security specialists
- Learned real-world experience from large enterprises implementing cloud security  

#### Lessons learned
- Cloud security requires a proactive, multi-layered approach
- Identity is the most important defense layer
- Logging, visibility, and automation must be prioritized
- IR playbooks and auto-response are essential—not optional  

#### Some event photos
![Event3](/images/4-EventParticipated/4.3-Event3/event3.jpg) 

> Overall, the event not only strengthened my cloud security foundation but also reshaped my mindset on designing secure architectures, adopting modern AWS best practices, and improving operational discipline across teams.
