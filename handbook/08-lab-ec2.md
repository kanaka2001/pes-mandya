# Chapter 08 — Lab: Amazon EC2 & Network/Application Security

> ⏰ 12:30 – 01:05 PM | 🧪 Hands-on lab

**By the end of this chapter you can:**
- Explain virtualization and why it powers the cloud
- Launch an EC2 instance
- Compare Security Groups and Network ACLs

---

## ⚙️ Virtualization: The Engine of Cloud

Virtualization lets one physical server run many isolated virtual machines. This lets providers share hardware efficiently among customers and create servers in minutes.

---

## 🖥️ Amazon EC2

**Amazon Elastic Compute Cloud (EC2)** provides resizable virtual servers.

| Term | Meaning |
|---|---|
| **AMI** | Template with the OS and software for an instance |
| **Instance type** | CPU, memory, and network size, for example `t3.micro` |
| **Key pair** | Credentials for secure login (SSH) |
| **EBS volume** | Block storage attached to an instance |
| **Security group** | Virtual firewall for the instance |

---

## 🛡️ Security Groups vs. NACLs

| Feature | Security Group | Network ACL |
|---|---|---|
| Level | Instance (network interface) | Subnet |
| State | **Stateful** (return traffic automatically allowed) | **Stateless** (return traffic must be allowed explicitly) |
| Rules | Allow only | Allow and deny |
| Evaluation | All rules evaluated | Rules evaluated in number order |
| Default | Denies all inbound | Default NACL allows all |

---

## 🧪 Lab 1: Launch an EC2 Instance

1. Open **EC2** in the Console and confirm the Region
2. Choose **Launch instance**
3. Name it `workshop-ec2-<yourname>`
4. AMI: **Amazon Linux** (Free Tier eligible)
5. Instance type: `t2.micro` or `t3.micro` (Free Tier eligible)
6. Key pair: create a new one or follow the facilitator's instruction
7. Network settings: choose the default VPC and create a security group allowing **SSH (22)** from **My IP** only. Add **HTTP (80)** if instructed
8. Keep the default storage
9. Choose **Launch instance**
10. Wait for **Instance state: Running** and **Status checks: 2/2 passed**
11. Note the public IPv4 address
12. (Optional) Connect using **EC2 Instance Connect**

---

## 🧪 Lab 2: Explore Security Groups and NACLs

1. Select your instance, open the **Security** tab, and view the inbound rules
2. Edit the inbound rules and observe how access changes
3. Open **VPC → Network ACLs** and view the default NACL rules
4. Compare with the security group, noting allow/deny and stateless differences

---

## 🧹 Clean Up

> ⚠️ **Terminate** your instance when finished, to avoid charges.

---

## 🛠️ Common Issues

| Problem | Likely cause |
|---|---|
| Cannot connect | Security group does not allow your IP or port |
| No public IP | Auto-assign public IP is disabled |
| Instance limit error | Account quota. Ask a facilitator |

---

## ✅ Chapter Checklist

- [ ] Launched an EC2 instance and saw it Running
- [ ] Reviewed its security group rules
- [ ] Viewed the default NACL
- [ ] Terminated the instance

---

> ✅ **Next up:**
> ### 👉 [Chapter 09 — AWS Builder Center & Well-Architected Framework](09-well-architected.md)
