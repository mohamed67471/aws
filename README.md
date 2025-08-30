# AWS Networking Project

## Overview
This project demonstrates how to design and implement a **highly available, secure, and scalable network architecture** on AWS using multiple availability zones.  
The architecture ensures reliability, fault tolerance, and controlled internet access.

---

## Architecture Diagram
<img width="940" height="722" alt="image" src="https://github.com/user-attachments/assets/5f0560a8-fc63-45dc-918b-88a590052037" />


---

## Components

### 1. VPC (Virtual Private Cloud)
- Provides an isolated network environment in AWS.
- Hosts all networking resources (subnets, gateways, servers).

### 2. Availability Zones (AZs)
- Two AZs are used to increase availability and fault tolerance.
- If one AZ goes down, the other can handle the traffic.

### 3. Public Subnets
- Contain **NAT Gateways** that provide internet access to private subnets.
- Each NAT Gateway is attached to an **Elastic IP (EIP)**.

### 4. Private Subnets
- Contain **Web Servers** that host the application.
- Do not have direct access to the internet for security reasons.

### 5. Internet Gateway (IGW)
- Allows inbound and outbound traffic between the VPC and the internet.
- Connected to the public subnets and the ALB.

### 6. Application Load Balancer (ALB)
- Distributes incoming user traffic across the web servers in both private subnets.
- Ensures fault tolerance and scalability.

---

## Traffic Flow
1. A user accesses the application over the internet.  
2. The request passes through the **Internet Gateway (IGW)** to the **Application Load Balancer (ALB)**.  
3. The ALB forwards the request to one of the **Web Servers** in the private subnets.  
4. If the web servers need to download packages or updates, they route through the **NAT Gateways** in the public subnets.  

---

## Security
- **Security Groups**:  
  - ALB allows inbound HTTP/HTTPS traffic from the internet.  
  - Web servers accept traffic only from the ALB.  
  - NAT Gateways allow outbound internet access only.  
- **Private Subnets**:  
  - Keep web servers isolated from direct internet access.  
- **Elastic IPs**:  
  - Provide consistent outbound IPs for NAT Gateways.  

---

## Key Learnings
- Multi-AZ design improves **high availability** and **fault tolerance**.  
- **NAT Gateways** secure private resources while still allowing outbound access.  
- **Application Load Balancer** improves scalability and ensures traffic is distributed evenly.  
- Managing **subnets, route tables, and security groups** is critical for AWS networking.  

---

## Future Improvements
- Add an **Auto Scaling Group** for web servers.  
- Integrate **CloudWatch** monitoring and alarms.  
- Use **AWS WAF (Web Application Firewall)** for enhanced security.  
