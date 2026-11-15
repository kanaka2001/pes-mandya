# Amazon VPC & Cloud Networking

**Time:** 11:20 – 11:50 AM (includes AWS Console walkthrough)

## Learning objectives

- Explain what a VPC is.
- Differentiate public and private subnets.
- Describe route tables, internet gateways, and load balancers.

## 4.1 What is a VPC?

A **Virtual Private Cloud (VPC)** is your own logically isolated network inside AWS. You control the IP range (CIDR block), subnets, routing, and gateways.

## 4.2 Building blocks

| Component | Purpose |
|---|---|
| **CIDR block** | The IP address range of the VPC, for example `10.0.0.0/16`. |
| **Subnet** | A slice of the VPC IP range, located in one AZ. |
| **Route table** | Rules that decide where network traffic goes. |
| **Internet Gateway (IGW)** | Connects the VPC to the internet. |
| **NAT Gateway** | Lets private subnets reach the internet outbound only. |
| **Load Balancer** | Distributes incoming traffic across multiple targets. |

## 4.3 Public vs. private subnets

| | Public subnet | Private subnet |
|---|---|---|
| Route to Internet Gateway | Yes | No |
| Direct internet access | Yes | No |
| Typical use | Web servers, load balancers | Databases, application servers |

A subnet is *public* only because its route table has a route to an Internet Gateway.

## 4.4 Example architecture

```
                 Internet
                    |
             [Internet Gateway]
                    |
   +----------------- VPC 10.0.0.0/16 ----------------+
   |                                                    |
   |  Public Subnet 10.0.1.0/24    Private Subnet 10.0.2.0/24
   |  [Load Balancer / Web]  --->  [App / Database]     |
   |                                                    |
   +----------------------------------------------------+
```

## 4.5 Load balancers

- **Application Load Balancer (ALB):** HTTP/HTTPS, layer 7.
- **Network Load Balancer (NLB):** TCP/UDP, layer 4, very high performance.
- Benefits: higher availability, health checks, even distribution of traffic.

## 4.6 Console walkthrough

Follow along as the facilitator demonstrates:

1. Open the **VPC** service in the AWS Console.
2. View the default VPC and its subnets.
3. Open **Route tables** and find the route to the Internet Gateway.
4. View the **Internet gateways** page.
5. Look at where **Load Balancers** are created (EC2 console).

> Space for your notes: ____________________________________

## Key takeaways

- A VPC is your private network in AWS.
- Route tables decide whether a subnet is public or private.

## Discussion questions

1. Why should a database sit in a private subnet?
2. What happens if one AZ fails and you have a load balancer across two?

---

[← Previous: AWS Fundamentals, Global Infrastructure & Service Models](03-aws-fundamentals.md) | [Home](README.md) | [Next: Transition, Q&A & Lab Readiness Check →](05-readiness-check.md)
