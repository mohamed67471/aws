# CloudWatch Monitoring & Logs

## Objective
Monitor EC2 metrics and logs using Amazon CloudWatch.

## Steps
1. Install CloudWatch Agent
   ```bash
   sudo yum install -y amazon-cloudwatch-agent
Configure Agent

bash
Copy code
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard
Start Agent

bash
Copy code
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl \
    -a start
