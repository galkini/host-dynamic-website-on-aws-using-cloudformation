![Alt text](/Dynamic_Web_Site_on_AWS_with_CloudFormation.png)

# DevOps Project: Dynamic Website on AWS

Welcome to the DevOps Project: Dynamic Website on AWS! This repository contains a reference diagram to deploy a dynamic website using AWS CloudFormation.

## Project Overview

This project demonstrates a comprehensive deployment of a dynamic website hosted on AWS using a variety of AWS services and best practices for reliability, security, and scalability.

### Key Features

- **Virtual Private Cloud (VPC):** Configured with both public and private subnets across two availability zones.
- **Internet Gateway:** Enables connectivity between VPC instances and the Internet.
- **Security Groups:** Serves as network firewall mechanisms.
- **Availability Zones:** Utilized for increased reliability and fault tolerance.
- **Public and Private Subnets:** Public subnets for infrastructure components like NAT Gateway and Application Load Balancer; private subnets for web server security.
- **EC2 Instances:** Hosted within private subnets for enhanced security.
- **NAT Gateway:** Allows instances in private subnets to access the internet.
- **Application Load Balancer:** Distributes web traffic evenly to an Auto Scaling Group of EC2 instances.
- **Auto Scaling Group:** Automatically manages EC2 instances to ensure availability, scalability, fault tolerance, and elasticity.
- **Certificate Manager:** Secures application communications.
- **Simple Notification Service (SNS):** Alerts about activities within the Auto Scaling Group.
- **Route 53:** Domain name registration and DNS configuration.

## Repository Contents

- **Reference Diagram**: A visual representation of the deployed architecture.

## Deployment Instructions

2. **Set Up AWS Environment**
   - Ensure you have the AWS CLI configured with appropriate access keys and region settings.

3. **Deploy the CloudFormation Stack**
   - Navigate to your AWS Management Console.
   - Upload the provided CloudFormation YAML templates from the `cloudformation` directory.
   - Follow the prompts to deploy the stack, ensuring you input necessary parameters where required (e.g., VPC ID, subnet IDs, etc.).

4. **Verify Deployments**
   - Check your VPC configurations, EC2 instances, and other AWS resources to ensure they have been correctly provisioned.
   - Ensure the website is accessible via the domain name registered and configured in Route 53.

## Monitoring and Alerts

- **SNS Configuration**: Ensure Simple Notification Service (SNS) is properly configured to receive alerts about activities within the Auto Scaling Group.

## Security

- **Certificate Manager**: SSL Certificates have been provisioned to secure application communications.

## Clean Up

To avoid unnecessary charges, ensure you delete the CloudFormation stack, which will automatically clean up all associated resources.
