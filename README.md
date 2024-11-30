# AWS Free Tier Terraform Project

## Overview
This Terraform project demonstrates a minimal AWS infrastructure setup utilizing Free Tier resources across multiple AWS services:
- RDS (MySQL)
- S3 Bucket
- EC2 Instance
- EBS Volume
- EFS File System
- IAM Roles and Policies

## Prerequisites
- Terraform (>= 1.0)
- AWS Account with Free Tier access
- AWS CLI configured with credentials

## Services Breakdown
1. **VPC**: Custom VPC with a single subnet
2. **IAM**: 
   - Role for EC2 
   - S3 access policy
3. **S3**: Bucket with random suffix
4. **EBS**: 1GB Volume
5. **EFS**: File system for persistent storage
6. **EC2**: t2.micro instance
7. **RDS**: MySQL database on db.t3.micro

## Important Considerations
- All resources are configured to maximize Free Tier eligibility
- Ensure you monitor AWS usage to stay within Free Tier limits
- Credentials and sensitive data are hardcoded for demonstration (NOT recommended for production)

## Setup Instructions
1. Clone this repository
2. Run `terraform init`
3. Run `terraform plan` to verify resources
4. Run `terraform apply`

## Cost Management
- Regularly check AWS billing console
- Set up billing alerts
- Destroy resources when not in use with `terraform destroy`

## Security Notes
- Replace hardcoded credentials in production
- Use AWS Secrets Manager for sensitive information
- Implement more restrictive IAM policies

## Potential Improvements
- Add network security groups
- Implement more granular IAM permissions
- Add encryption for sensitive resources

## Cleanup
To avoid unexpected charges, always run `terraform destroy` when resources are no longer needed.
