# AWS Workshop: Deploying Highly Available WordPress with Terraform

## Overview
This repository demonstrates how to deploy a highly available WordPress application on AWS using Terraform. We'll leverage various AWS services to create a robust and scalable architecture.
### [Link to AWS Workshop](https://catalog.workshops.aws/terraform101/en-US) 

## Table of Contents
- Introduction
- Architecture
- Tools Used
- Getting Started
- Deployment Steps
- Troubleshooting

## Introduction
In this repository, we'll set up a WordPress site with the following features:
- **High Availability:** The application will be distributed across multiple Availability Zones (AZs) to ensure resilience.
- **Auto-Scaling:** We'll configure auto-scaling based on CPU utilization to handle varying traffic loads.
- **Database:** We'll use Amazon RDS (Relational Database Service) for our MySQL database.
- **Storage:** Amazon S3 and Amazon EFS (Elastic File System) will be used for media storage.
- **Content Delivery:** CloudFront will accelerate content delivery using edge locations.

## Architecture
Our architecture will look like this:
![Architecture Diagram](https://static.us-east-1.prod.workshops.aws/public/3a811ff3-2be5-4d8f-80a8-85b21ca5b5e4/static/images/00/p01-01-workshop-architecture.png)
Diagram Source: https://catalog.workshops.aws/terraform101/en-US/0-introduction

- **VPC (Virtual Private Cloud):** We'll create a custom VPC with public and private subnets.
- **EC2 Instances:** WordPress will run on EC2 instances in the private subnet.
- **RDS:** Multi-AZ MySQL database for WordPress data.
- **S3:** Storing media files (images, videos, etc.).
- **EFS:** Shared storage for WordPress files.
- **SSM (Systems Manager):** Parameter Store for securely storing configuration data.
- **Secrets Manager:** Storing database credentials.
- **ACM (AWS Certificate Manager):** SSL certificates for HTTPS.
- **CloudFront:** Content delivery via CDN.

## Tools Used
- **Terraform:** Infrastructure as Code (IaC) tool for provisioning AWS resources.
- **AWS CLI:** Command-line interface for managing AWS services.
- **GitHub:** Version control and collaboration platform.
- **Your Preferred Text Editor/IDE:** For editing Terraform files.

## Getting Started
1. Clone this repository to your local machine.
2. Install Terraform and the AWS CLI.
3. Set up your AWS credentials.

## Deployment Steps
1. Run `terraform init` to initialize the Terraform configuration.
2. Run `terraform plan` to review the changes.
3. Run `terraform apply` to create the infrastructure.
4. Access your WordPress site via the provided URL.

## Troubleshooting
If you encounter any issues during deployment, refer to the troubleshooting section in the workshop documentation.

Happy coding! 🚀
