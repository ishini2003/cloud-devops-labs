# Terraform Lab 002 - Create AWS Security Group

## Objective

Create an AWS Security Group in the default VPC using Terraform.

## Requirements

- Region: us-east-1
- Security Group Name: devops-sg
- Description: Security group for Nautilus App Servers

### Inbound Rules

| Protocol | Port | Source |
|----------|------|--------|
| HTTP | 80 | 0.0.0.0/0 |
| SSH | 22 | 0.0.0.0/0 |

## Terraform Concepts Learned

- AWS Security Groups
- Default VPC Data Source
- Ingress Rules
- Egress Rules
- Infrastructure as Code (IaC)

## Files

- `main.tf` - Terraform configuration
- `README.md` - Lab documentation

## Commands Used

```bash
terraform init
terraform plan
terraform apply
```

## Outcome

Successfully created an AWS Security Group named **devops-sg** in the default VPC with HTTP and SSH access configured.