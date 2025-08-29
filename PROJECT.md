# AWS Networking Project

## Project Overview
This project implements a highly available, secure, and scalable network architecture on AWS using multiple Availability Zones (AZs). It demonstrates best practices in networking, security, and fault tolerance.

---

## Architecture Components

### VPC (Virtual Private Cloud)
An isolated network environment for your AWS resources.

### Availability Zones (AZs)
Two AZs are used to ensure high availability and fault tolerance.

### Public Subnets
- Contain NAT Gateways and provide external access.
- Each NAT Gateway is associated with an Elastic IP (EIP) for stable internet connectivity.

### Private Subnets
- Contain Web Servers that host the application.
- Cannot directly access the internet; route outbound traffic via NAT Gateways in public subnets.

### Internet Gateway (IGW)
Provides internet access for public subnets and the Application Load Balancer (ALB).

### Application Load Balancer (ALB)
- Distributes incoming traffic across web servers in private subnets.
- Ensures fault tolerance and scalability.

---

## Traffic Flow
1. User traffic from the internet reaches the ALB through the IGW.
2. The ALB routes requests to web servers in private subnets across both AZs.
3. Web servers access the internet for updates via NAT Gateways in public subnets.

---

## Security Features
- **Security Groups**: Control inbound/outbound traffic for EC2 instances, NAT Gateways, and the ALB.
- **Private Subnets**: Web servers are isolated from direct internet access.
- **Elastic IP (EIP) for NAT Gateways**: Ensures stable public IPs for outbound traffic.

---

## Key Learnings
- Multi-AZ architecture improves availability and fault tolerance.
- NAT Gateways provide secure internet access for private subnets.
- ALB ensures load balancing and redundancy across web servers.
- Proper management of security groups and subnets is essential for AWS networking security.

---

## Architecture Diagram


![Architecture Diagram]<img width="940" height="722" alt="image" src="https://github.com/user-attachments/assets/6e90c6c1-9297-411e-b04c-6cd9a3645647" />

