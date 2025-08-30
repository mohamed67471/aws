# EC2 Setup (Backend Servers)

## Step 1: Launch EC2 Instances
1. Go to **EC2 → Launch Instance**.
2. AMI: Amazon Linux 2 or Ubuntu.
3. Instance type: t2.micro (free tier eligible).
4. Network: Launch into **private subnets**.
5. Security group: Attach **EC2 security group** (only allows traffic from ALB SG).

---

## Step 2: Connect to EC2
- Use **Bastion Host** or Session Manager to access private EC2.

---

## Step 3: Install Web Server
For Amazon Linux 2:
#!/bin/bash 
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
