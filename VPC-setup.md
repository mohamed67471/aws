# VPC Setup

## Objective
Create a custom VPC with public and private subnets, configure routing and internet access.

## Steps

1. **Create a VPC**
   - Name: `MyVPC`
   - CIDR block: `10.0.0.0/16`

2. **Create Subnets**
   - Public Subnet: `10.0.1.0/24`
   - Private Subnet: `10.0.2.0/24`

3. **Internet Gateway (IGW)**
   - Attach IGW to the VPC
   - Update route table for public subnet

4. **NAT Gateway (NGW)**
   - Launch in public subnet
   - Update private subnet route table to use NAT Gateway for internet access
