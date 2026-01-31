# Lab: EC2 Web Server

## Objective
Launch an EC2 instance and host a simple web page accessible from the internet.

## AWS Services Used
- EC2
- IAM
- VPC
- Security Groups

## Architecture Overview
User → Internet → EC2 (Web Server)

## Steps

### 1. Launch EC2 Instance
- AMI: Amazon Linux 2
- Instance type: t2.micro (Free Tier)
- Network: Default VPC
- Subnet: Public subnet
- Auto-assign Public IP: Enabled

### 2. Configure Security Group
Inbound rules:
- SSH (22) from your IP
- HTTP (80) from 0.0.0.0/0

### 3. Connect to Instance
Use SSH with your key pair:
```bash
ssh -i your-key.pem ec2-user@<public-ip>
## Validation
- Confirmed Apache running via systemctl
- Verified localhost returns HTTP 200
- Verified public access via browser

## Security Configuration
- SSH restricted to my IP
- HTTP (80) open to the internet via security group

## Clean-up Considerations
- Instance can be stopped or terminated to avoid charges
- Security group rules should be restricted in production
