# Implementing a Load-Balanced Calculator Application in AWS

A simple calculator web application across two AWS availability zones using an Application Load Balancer (ALB) for high availability and scalability. The application is built with HTML, CSS, and JavaScript, hosted on EC2 instances.

## Steps to run:

1. Prerequisites:
   - AWS Console
   - AWS CLI configured on your local machine.
   - SSH key pair for EC2 access

2.Infrastructure setup

Step 1: Create a VPC

 - click on vpc and more with 2 availabilty zones
 
Step 2: Launch 2 EC2 Instances  

- in instance 1 add userdata 1
 
- in instance 2 add userdata 2

Step 3:Application Load Balancer

 - Create an Application Load Balancer

 - Configure it to listen on HTTP (port 80).

 - Select both subnets (us-east-1a, us-east-1b).
 
 - Create a target group named CalculatorTG with HTTP health checks on /index.html.
 
 - Register the two EC2 instances in the target group.

Step 4: Test the Application
 
 - Obtain the ALB DNS name from the AWS Console.
