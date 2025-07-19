# Approach Documentation

## Part 1: Infrastructure Provisioning

- Used **Terraform** to provision cloud infrastructure.
- Created:
  - VPC with public and private subnets
  - EC2 instances (simulated)
  - RDS for PostgreSQL (with backup retention)
  - Security Groups and IAM roles
  - Application Load Balancer
- Used `variables.tf`, `outputs.tf`, and `main.tf` to modularize configuration.
- Followed best practices:
  - Clear variable usage
  - Output key resources
  - Future-ready for remote state (e.g., S3 backend)

## Part 2: Deployment Automation

- Used **GitHub Actions** for CI/CD pipeline.
- Workflow includes:
  - PR-based testing (placeholder)
  - Docker image build and simulated push
  - Staging deployment (mocked)
  - Manual prod approval gate
  - Vulnerability scan steps (planned via Trivy or similar)
  - Notifications via Slack/email placeholder

## Part 3: Monitoring and Logging

- Simulated Prometheus config for:
  - Node Exporter (CPU, memory, etc.)
  - Application metrics endpoint
- Created sample **Grafana dashboard** JSON with:
  - CPU usage
  - Request latency
- Created centralized log samples:
  - `app.log`, `access.log`, `system.log`

## Part 4: Documentation & Best Practices

- Wrote clear `README.md` with:
  - Setup steps
  - Architecture summary
  - Security recommendations
  - Cost optimization strategies
- Secret management suggestion:
  - Use AWS Secrets Manager or GitHub Encrypted Secrets
- Backup strategy:
  - Enabled RDS backups via Terraform
  - Suggested log backups to S3

---
> The entire setup is designed to simulate a realistic DevOps pipeline while being light enough to complete within the assignment timeline.
