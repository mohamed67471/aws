# Security Groups Setup

This document outlines the security groups created for the **AWS ALB + EC2 Project**.

---

## 1. Application Load Balancer (ALB) Security Group
- **Purpose:** Allow inbound traffic from the internet to the ALB.  
- **Inbound Rules:**
  - HTTP (80) → 0.0.0.0/0
  - HTTPS (443) → 0.0.0.0/0  
- **Outbound Rules:**
  - Allow all outbound (default).

---

## 2. Backend EC2 Instances Security Group
- **Purpose:** Protect EC2s while allowing traffic only from the ALB.  
- **Inbound Rules:**
  - HTTP (80) → Source: ALB Security Group
  - SSH (22) → Source: Your IP address (for administration only)  
- **Outbound Rules:**
  - Allow all outbound (default).

---

## 3. Optional Bastion Host Security Group
- **Purpose:** Secure access to private EC2 instances.  
- **Inbound Rules:**
  - SSH (22) → Source: Your IP address  
- **Outbound Rules:**
  - Allow all outbound (default).  
- **Note:** If a Bastion Host is not deployed, direct SSH should only be restricted to your IP for the backend EC2s.

---

## Security Best Practices
1. **Least Privilege:** Only open the required ports.  
2. **Segmentation:** ALB receives traffic from the internet, EC2s only trust ALB traffic.  
3. **Restricted SSH:** Limit to specific IPs, never open 22 to the world.  
4. **Monitoring:** Use AWS CloudWatch or VPC Flow Logs to monitor suspicious traffic.  

---
✅ This ensures only the ALB communicates with backend instances, while administration is limited to trusted IPs.
