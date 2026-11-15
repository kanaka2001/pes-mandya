# AWS Fundamentals, Global Infrastructure & Service Models

**Time:** 11:00 – 11:20 AM

## Learning objectives

- Identify the essential characteristics of cloud computing.
- Describe the AWS Global Infrastructure.
- Distinguish deployment models and service models.

## 3.1 Essential cloud characteristics

- On-demand self-service
- Broad network access
- Resource pooling
- Rapid elasticity
- Measured service

## 3.2 AWS Global Infrastructure

| Component | Description |
|---|---|
| **Region** | A geographic area containing multiple isolated Availability Zones. |
| **Availability Zone (AZ)** | One or more data centers with independent power and networking, within a Region. |
| **Edge Locations** | Sites used by services such as CloudFront to deliver content with low latency. |

Why it matters: spreading workloads across AZs improves availability and fault tolerance. Choosing a Region near users reduces latency and can help meet data-residency requirements.

## 3.3 Deployment models

- **Public cloud:** resources run on the provider's infrastructure (for example, AWS).
- **Private cloud:** infrastructure used by a single organization.
- **Hybrid cloud:** on-premises and cloud combined.

## 3.4 Core service models

| Model | You manage | Provider manages | Example |
|---|---|---|---|
| **IaaS** | OS, apps, data | Hardware, virtualization | Amazon EC2 |
| **PaaS** | Apps, data | Platform, OS, infrastructure | AWS Elastic Beanstalk |
| **SaaS** | Just use it | Everything | Amazon WorkMail, Gmail |

## 3.5 Emerging models

- **FaaS (Function as a Service):** run code without managing servers, for example AWS Lambda.
- **CaaS (Containers as a Service):** managed container platforms, for example Amazon ECS and EKS.
- **DBaaS (Database as a Service):** managed databases, for example Amazon RDS and DynamoDB.
- **DaaS (Desktop as a Service):** cloud-hosted virtual desktops, for example Amazon WorkSpaces.

## 3.6 Shared Responsibility Model

- **AWS:** security *of* the cloud (hardware, facilities, core services).
- **Customer:** security *in* the cloud (data, access, configuration).

## Key takeaways

- A Region contains multiple AZs.
- Higher-level service models mean less for you to manage.

## Discussion questions

1. Which service model would you pick for a college website? Why?
2. Why might a company choose two Regions?

---

[← Previous: Cloud Computing: Before & After the Cloud](02-cloud-history.md) | [Home](README.md) | [Next: Amazon VPC & Cloud Networking →](04-vpc-networking.md)
