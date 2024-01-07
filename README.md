# aws-terraform-project
Project Title: Multi-AZ Web Application Deployment with Terraform

Description:
This Terraform project orchestrates the creation of a resilient web application infrastructure on AWS. It sets up a Virtual Private Cloud (VPC) with two subnets spread across different availability zones in the us-east-1 region. The architecture includes:

VPC Setup: Defines a custom VPC with specified CIDR block.
Subnets: Creates two subnets (us-east-1a and us-east-1b) within the VPC to distribute resources across availability zones for fault tolerance.
Internet Gateway: Establishes an internet gateway for public internet access.
Route Tables: Configures route tables and associations for public internet access via the internet gateway.
Security Group: Defines a security group (Web-sg) with rules allowing HTTP and SSH traffic.
S3 Bucket: Creates an AWS S3 bucket named abhisheksterraform2023project.
EC2 Instances: Deploys two EC2 instances (webserver1 and webserver2) in separate subnets, each with its own user data script.
Application Load Balancer (ALB): Sets up an ALB (myalb) with listeners and forwards traffic to a target group.
Target Group: Defines a target group (myTG) for routing incoming HTTP traffic to EC2 instances, and it performs health checks on the instances.
ALB Listener: Configures an ALB listener that forwards incoming HTTP traffic on port 80 to the target group.
This Terraform script automates the deployment of a scalable and highly available web application environment, distributing traffic across multiple instances and ensuring redundancy by utilizing multiple availability zones within the selected region.
