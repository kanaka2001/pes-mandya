# Amazon EC2 & Network/Application Security

**Time:** 12:30 – 01:05 PM | **Hands-on lab**

## Learning objectives

- Explain virtualization and why it powers the cloud.
- Launch an EC2 instance.
- Compare Security Groups and Network ACLs.

## 8.1 Virtualization: the engine of cloud

Virtualization lets one physical server run many isolated virtual machines. This makes it possible to share hardware among customers efficiently and to create servers in minutes.

## 8.2 Amazon EC2

**Amazon Elastic Compute Cloud (EC2)** provides resizable virtual servers.

| Term | Meaning |
|---|---|
| **AMI** | Template with the OS and software for an instance. |
| **Instance type** | CPU, memory, and network size, for example `t3.micro`. |
| **Key pair** | Credentials for secure login (SSH). |
| **EBS volume** | Block storage attached to an instance. |
| **Security group** | Virtual firewall for the instance. |

## 8.3 Security Groups vs. NACLs

| Feature | Security Group | Network ACL |
|---|---|---|
| Level | Instance (network interface) | Subnet |
| State | **Stateful** (return traffic automatically allowed) | **Stateless** (must allow return traffic explicitly) |
| Rules | Allow only | Allow and deny |
| Evaluation | All rules evaluated | Rules evaluated in number order |
| Default | Denies all inbound | Default NACL allows all |

## 8.4 Lab: launch an EC2 instance

1. Open **EC2** in the Console and confirm the Region.
2. Choose **Launch instance**.
3. Name it `workshop-ec2-<yourname>`.
4. Choose an AMI: **Amazon Linux** (Free Tier eligible).
5. Choose an instance type: `t2.micro` or `t3.micro` (Free Tier eligible).
6. Key pair: create a new one or proceed as directed by the facilitator.
7. Network settings: choose the default VPC and create a security group allowing **SSH (22)** from **My IP** only. Add **HTTP (80)** if instructed.
8. Keep the default storage.
9. Choose **Launch instance**.
10. Wait for **Instance state: Running** and **Status checks: 2/2 passed**.
11. Note the public IPv4 address.
12. (Optional) Connect using **EC2 Instance Connect**.

## 8.5 Lab: explore Security Groups and NACLs

1. Select your instance, open the **Security** tab, and view the inbound rules.
2. Edit the inbound rules and observe how access changes.
3. Open **VPC > Network ACLs** and view the default NACL rules.
4. Compare with the security group, noting the allow/deny and stateless differences.

## Clean up

- **Terminate** your instance when finished, to avoid charges.

## Common issues

| Problem | Likely cause |
|---|---|
| Cannot connect | Security group does not allow your IP or port. |
| No public IP | Auto-assign public IP disabled. |
| Instance limit error | Account quota. Ask a facilitator. |

## Key takeaways

- EC2 provides virtual servers on demand.
- Security Groups are stateful and instance-level. NACLs are stateless and subnet-level.

---

[← Previous: Amazon S3 (Simple Storage Service)](07-lab-s3.md) | [Home](README.md) | [Next: AWS Builder Center & Well-Architected Framework →](09-well-architected.md)
