# AWS Networking Assignment

## Objective
Create a custom VPC with both public and private subnets, configure internet access, and deploy EC2 instances with secure segmentation.

---

## Repository Structure

AWS-Networking-Assignment/
│
├─ README.md # This file
├─ VPC-setup.md # Steps to create VPC, subnets, IGW, NAT Gateway
├─ EC2-setup.md # Public & Private EC2 setup
├─ Bastion-Host.md # Optional jump box setup
├─ CloudWatch.md # CloudWatch monitoring & logs steps
├─ diagrams/
│ └─ vpc-diagram.png # Architecture diagrams
└─ scripts/
└─ cloudwatch-install.sh # CloudWatch installation script


---

## Assignment Steps

### 1. VPC & Subnets
- Created a custom VPC.
- Added at least one public and one private subnet.
- Configured route tables for correct traffic flow.

### 2. Internet & NAT Gateway
- Attached an Internet Gateway (IGW) to the VPC.
- Deployed a NAT Gateway (NGW) in the public subnet to allow private instances outbound internet access.

### 3. EC2 Instances
- Launched a public EC2 instance with internet access.
- Launched a private EC2 instance with no direct internet access.
- Configured security groups to allow SSH access only via the public instance (Bastion Host).

### 4. Routing & Security
- Configured route tables for both public and private subnets.
- Restricted direct SSH access to private instances.

### 5. Bonus: Bastion Host
- Optional setup for a jump box to access private instances securely.

### 6. CloudWatch Monitoring
- Installed and configured Amazon CloudWatch Agent.
- Monitors metrics and logs from EC2 instances.

---

## Notes
- All scripts and diagrams are included in the respective folders.
- Ensure you have the correct IAM roles for CloudWatch and EC2 access.

---





