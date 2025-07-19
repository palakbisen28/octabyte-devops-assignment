# octabyte-devops-assignment
DevOps assignment for Octa Byte AI Pvt Ltd

## Infrastructure Setup

Provisioning is done using Terraform (AWS targeted):

- VPC with public & private subnets
- EC2 for app hosting
- RDS (PostgreSQL) for DB
- Security Groups
- Application Load Balancer
- Output + Variables + State mgmt

 `/terraform/` for full setup.

---

##  CI/CD Pipeline

Using GitHub Actions to automate:

- PR testing
- Docker image build + push
- Staging deployment
- Manual prod approval step
- Vulnerability scanning placeholder

See `.github/workflows/ci-cd.yml`

---

##  Monitoring & Logging

Basic observability setup:

- `Prometheus` config for app + infra metrics
- `Grafana` dashboard (JSON export included)
- Centralized logs: `app.log`, `access.log`, `system.log`

➡All under `/monitoring/`

---

## Security Considerations

- **Secrets:** Simulated use of `.env` (not committed) + suggestion to use [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) or GitHub Encrypted Secrets.
- **IAM:** Fine-grained roles (not hardcoded credentials)
- **State Mgmt:** Remote state suggested (e.g., S3 + DynamoDB)

---

## Cost Optimization

- Use t2.micro/t3.micro for test infra
- Enable auto-scaling
- Reserved Instances for DB in production
- Turn off non-prod resources during idle time

---

## Backup Strategy

- Simulate RDS automatic backups via `backup_retention_period` in Terraform.
- Suggest: Daily snapshots + S3 archiving
- Log backups to Amazon S3

---

##  How to Run (Simulated)

```bash
# Navigate to terraform folder
cd terraform/

# Init and plan
terraform init
terraform plan

# Apply (for real usage)
# terraform apply
