# Implementing a Load-Balanced Calculator Application in AWS

A simple calculator web application across two AWS availability zones using an Application Load Balancer (ALB) for high availability and scalability. The application is built with HTML, CSS, and JavaScript, hosted on EC2 instances.

## Steps to run:

1. Prerequisites:
   - AWS Console
   - AWS CLI configured on your local machine.
   - SSH key pair for EC2 access

2.Infrastructure setup

Step 1: Create a VPC

1. Log in to the AWS Management Console.

2. Navigate to the VPC service.
  
3. Create a VPC with CIDR block 10.0.0.0/16.
  
4. Name it CalculatorVPC.
  
5. Enable DNS hostnames and DNS resolution.

Step 2: Create Subnets

1. Create two public subnets in different availability zones (e.g., us-east-1a, us-east-1b):
   
• Subnet 1: 10.0.1.0/24 in us-east-1a.

• Subnet 2: 10.0.2.0/24 in us-east-1b.

3. Associate an Internet Gateway with the VPC.
  
4. Update the route table to route 0.0.0.0/0 to the Internet Gateway.

Step 3: Launch EC2 Instances   
