# AWS Projects

This folder contains two hands-on AWS networking projects completed as part of my learning journey.  
Each project is isolated in its own branch for clarity.  

---

## 📌 [Network Assignment 1](https://github.com/mohamed67471/aws/tree/network-assignment-1) 

**Title:** AWS Networking Assignment  

**Objective:**  
Design and implement a custom VPC with public and private subnets, secure EC2 deployments, and monitoring with CloudWatch.  

**Key Features:**
- Custom VPC with segmented public/private subnets  
- Internet Gateway (IGW) and NAT Gateway setup  
- Public and private EC2 instances with secure access  
- Bastion Host for jump-box SSH (optional)  
- Route table configuration for traffic control  
- CloudWatch setup for monitoring  

**Repository Structure (branch `network-assignment-1`):**
- `README.md` – Overview of the assignment  
- `VPC-setup.md` – VPC and subnet configuration steps  
- `EC2-setup.md` – EC2 setup guide (public/private)  
- `Bastion-Host.md` – Bastion/jump box setup  
- `CloudWatch.md` – Monitoring setup steps   
-  

---

## 📌 [Network Assignment 2](https://github.com/mohamed67471/aws/tree/network-assignment-2)

**Title:** AWS Load Balancer & High Availability Project  

**Objective:**  
Deploy an application across multiple availability zones with high availability and fault tolerance using an Application Load Balancer (ALB).  

**Key Features:**
- Application Load Balancer (ALB) setup  
- Target groups with EC2 instances across AZs  
- Health checks and failover validation  
- Auto-scaling considerations  
- Security groups for restricted access  
- Architecture diagram included  

**Repository Structure (branch `network-assignment-2`):**
- `README.md` – Overview of the assignment  
- `ALB-setup.md` – Steps for ALB and target groups  
- `EC2-setup.md` – Backend EC2 configuration  
- `Security-Groups.md` – Firewall rules  
- 

---

## 🔗 How to View the Projects
Each project lives in a separate branch:  

- [Network Assignment 1](https://github.com/mohamed67471/aws/tree/network-assignment-1) 
- [Network Assignment 2](https://github.com/mohamed67471/aws/tree/network-assignment-2)  

Clone the repo and switch to the desired branch:  

```bash
# Example: Checkout project 1
git checkout network-assignment-1

# Example: Checkout project 2
git checkout network-assignment-2





