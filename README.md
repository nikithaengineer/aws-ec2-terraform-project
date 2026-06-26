# AWS EC2 Provisioning with Terraform

## Overview
This project uses Terraform to provision an AWS EC2 instance along with a security group, demonstrating Infrastructure as Code (IaC) principles for automated, repeatable cloud infrastructure deployment.

## Architecture
- *AWS EC2* — t2.micro Ubuntu instance
- *Security Group* — allows inbound SSH (22) and HTTP (80) traffic
- *Terraform* — manages provisioning, state, and teardown

## Tools Used
- Terraform
- AWS CLI
- AWS EC2, Security Groups, IAM

## How to Run
1. Configure AWS CLI: aws configure
2. Initialize Terraform: terraform init
3. Review the execution plan: terraform plan
4. Apply the configuration: terraform apply
5. Destroy resources when done: terraform destroy


## SCREENSHOT
![EC2 Instance Running] (Screenshot.png)

## Files
- main.tf — defines the EC2 instance and security group
- variable.tf — input variables (region, instance type, key name)
- outputs.tf — outputs the instance's public IP
- terraform.tfvars — local variable values (not committed, contains key name)

## Key Learnings
- Hands-on experience with Terraform's declarative syntax and state management
- Understanding of AWS security group rules and EC2 provisioning
- Practiced safe IaC practices (excluding state files and secrets from version control)

## Next Steps
- Add GitHub Actions for automated CI/CD deployment
- Migrate to EKS for container orchestration
- Add CloudWatch monitoring
