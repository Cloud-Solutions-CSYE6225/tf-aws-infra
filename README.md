# tf-aws-infra
# Terraform Continuous Integration

This Terraform project is designed to create an AWS Virtual Private Cloud (VPC) with multiple public and private subnets across different availability zones. The infrastructure is defined as code using Terraform, making it reusable and scalable for different environments.

## Introduction
The CI pipeline is triggered for every pull request to the main branch. It ensures that:

Terraform files are properly formatted using terraform fmt.
The configuration is syntactically valid using terraform validate.
The pull request cannot be merged unless the checks pass successfully.

## CI Workflow Overview
steps in the Workflow
Checkout Code: The workflow checks out the repository code.
Terraform Setup: The workflow installs Terraform CLI using the hashicorp/setup-terraform action.
Terraform Init: Initializes Terraform, downloading necessary providers and modules.
Terraform Formatting Check: Runs terraform fmt -check -recursive to ensure all .tf files are formatted according to Terraform standards.
Terraform Validation: Runs terraform validate to check for syntax errors or configuration issues.

## Branch Protection
To enforce code quality and prevent broken configurations from being merged into the main branch, GitHub branch protection rules have been enabled. This means that:

A pull request cannot be merged unless the Terraform CI checks pass.
The status checks required for merging include terraform fmt and terraform validate.
This ensures that all pull requests are validated and formatted properly before merging.


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


