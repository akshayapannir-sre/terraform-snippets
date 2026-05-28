# Terraform Snippets & Modules

> Reusable Terraform modules and snippets for AWS infrastructure,
> based on real production IaC managing infrastructure across 2 companies.

---

## 📁 Structure

```
terraform-snippets/
├── modules/
│   ├── vpc/
│   ├── ec2/
│   ├── eks/
│   ├── rds/
│   └── iam/
├── snippets/
│   ├── s3-backend.tf
│   ├── security-group.tf
│   ├── alb.tf
│   └── ecr.tf
├── examples/
│   ├── full-vpc-setup/
│   └── eks-cluster/
└── README.md
```

---

## 📦 Modules

| Module | Description |
|---|---|
| [vpc](modules/vpc/) | Production VPC with public/private subnets, NAT gateway |
| [ec2](modules/ec2/) | EC2 instance with IAM role, SG, EBS |
| [eks](modules/eks/) | EKS cluster with managed node groups |
| [rds](modules/rds/) | RDS PostgreSQL with multi-AZ, automated backups |
| [iam](modules/iam/) | IAM roles and policies with least privilege |

---

## ⚡ Quick Snippets

| Snippet | Use Case |
|---|---|
| [s3-backend.tf](snippets/s3-backend.tf) | Remote state with S3 + DynamoDB lock |
| [security-group.tf](snippets/security-group.tf) | Common SG patterns |
| [alb.tf](snippets/alb.tf) | Application Load Balancer setup |
| [ecr.tf](snippets/ecr.tf) | ECR repo with lifecycle policy |

---

## 💡 Based On Real Production IaC

- Authored Terraform for 2 companies as sole IaC engineer
- Manages VPC, Kubernetes, Jenkins, Vault, GitLab, all microservices
- GCP → AWS full infrastructure migration via Terraform
- Remote state management with S3 backend + DynamoDB locking
