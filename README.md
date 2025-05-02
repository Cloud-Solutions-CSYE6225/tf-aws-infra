# tf-aws-infra
# Terraform Continuous Integration

## Introduction of terraform
This Terraform project is designed to create an AWS Virtual Private Cloud (VPC) with multiple public and private subnets across different availability zones. The infrastructure is defined as code using Terraform, making it reusable and scalable for different environments.

## Introduction
The CI pipeline is triggered for every pull request to the main branch. It ensures that:

Terraform files are properly formatted using terraform fmt.
The configuration is syntactically valid using terraform validate.
The pull request cannot be merged unless the checks pass successfully.


## Prerequisites for terraform


Before proceeding, ensure you have the following:


- AWS account
- AWS CLI installed
- Terraform CLI installed

Initialize Terraform:
   ```bash
   terraform init
   ```

Validate the configuration:
   ```bash
   terraform validate
   ```

Plan infrastructure changes:
   ```bash
   terraform plan
   ```

Apply the changes to create VPC and subnets:
   ```bash
   terraform apply
   ```

### Checking State

Check the state of your infrastructure using:
```bash
terraform show
