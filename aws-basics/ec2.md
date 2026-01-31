# Amazon EC2 (Elastic Compute Cloud)

EC2 provides resizable virtual servers (instances) in the cloud.
It allows you to run applications without owning physical hardware.

## What EC2 is used for
- Hosting web servers
- Running backend applications
- Batch processing and compute workloads
- Temporary or scalable compute needs

## Core EC2 concepts
- **Instance**: A virtual server
- **AMI (Amazon Machine Image)**: Template for the instance OS and software
- **Instance Type**: Defines CPU, memory, and networking capacity
- **Key Pair**: Used for secure SSH access
- **Security Group**: Virtual firewall controlling inbound and outbound traffic

## How EC2 fits into an architecture
- Usually placed inside a VPC
- Often sits behind a load balancer
- Commonly connects to databases or S3

## Notes
- Instances can be stopped, started, or terminated
- You pay for running time and instance size
- Security groups are stateful

