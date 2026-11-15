# Chapter 03 — AWS Fundamentals, Global Infrastructure & Service Models

> ⏰ 11:00 – 11:20 AM | 📖 Theory

**By the end of this chapter you can:**
- Identify the essential characteristics of cloud computing
- Describe the AWS Global Infrastructure
- Distinguish deployment models and service models

---

## 🔑 Essential Cloud Characteristics

- On-demand self-service
- Broad network access
- Resource pooling
- Rapid elasticity
- Measured service

---

## 🌍 AWS Global Infrastructure

| Component | Description |
|---|---|
| 🗺️ **Region** | A geographic area containing multiple isolated Availability Zones |
| 🏭 **Availability Zone (AZ)** | One or more data centers with independent power and networking, within a Region |
| 📡 **Edge Locations** | Sites used by services such as CloudFront to deliver content with low latency |

> 💡 Spreading workloads across AZs improves availability. Choosing a Region near your users reduces latency and can help meet data-residency requirements.

---

## 🏗️ Deployment Models

- **Public cloud:** resources run on the provider's infrastructure (for example, AWS)
- **Private cloud:** infrastructure used by a single organization
- **Hybrid cloud:** on-premises and cloud combined

---

## 🧱 Core Service Models

| Model | You manage | Provider manages | Example |
|---|---|---|---|
| **IaaS** | OS, apps, data | Hardware, virtualization | Amazon EC2 |
| **PaaS** | Apps, data | Platform, OS, infrastructure | AWS Elastic Beanstalk |
| **SaaS** | Just use it | Everything | Amazon WorkMail, Gmail |

---

## ✨ Emerging Models

| Model | Meaning | AWS example |
|---|---|---|
| **FaaS** | Run code without managing servers | AWS Lambda |
| **CaaS** | Managed container platforms | Amazon ECS, EKS |
| **DBaaS** | Managed databases | Amazon RDS, DynamoDB |
| **DaaS** | Cloud-hosted virtual desktops | Amazon WorkSpaces |

---

## 🤝 Shared Responsibility Model

- **AWS:** security *of* the cloud (hardware, facilities, core services)
- **Customer:** security *in* the cloud (data, access, configuration)

---

## 💬 Discussion

1. Which service model would you pick for a college website? Why?
2. Why might a company choose two Regions?

---

## ✅ Chapter Checklist

- [ ] I can explain Region, AZ, and Edge Location
- [ ] I can tell IaaS, PaaS, and SaaS apart
- [ ] I know what FaaS, CaaS, DBaaS, and DaaS mean

---

> ✅ **Next up:**
> ### 👉 [Chapter 04 — Amazon VPC & Cloud Networking](04-vpc-networking.md)
