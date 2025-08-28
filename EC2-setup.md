# EC2 Instances Setup

## Public EC2
- Instance type: `t2.micro`
- AMI: Amazon Linux 2
- Subnet: Public
- Security Group: Allow SSH from your IP, HTTP/HTTPS
- Key pair: `ec2log.pem`

## Private EC2
- Instance type: `t2.micro`
- AMI: Amazon Linux 2
- Subnet: Private
- Security Group: Allow SSH only from Public EC2 SG
- Key pair: Same as public (copied securely)

## Notes
- Test connectivity: SSH into public EC2 → then into private EC2
- Ensure private EC2 has **no direct internet access**
