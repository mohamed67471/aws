 Bastion Host (Jump Box) Setup

## Objective
Securely access private instances via a public EC2 (Bastion Host).

## Steps
1. Launch an EC2 in the public subnet (if not already done)
2. Assign a security group that allows SSH from your IP
3. Configure private EC2 security group to allow SSH from Bastion Host SG
4. SSH example:
ssh -i /path/to/key.pem -J ec2-user@Public-IP ec2-user@Private-IP

vbnet
Copy code

## Notes
- Bastion Host is optional but recommended for security.
- Do **not** expose private EC2 to the internet.
