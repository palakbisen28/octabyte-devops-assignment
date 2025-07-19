# Challenges Faced & Resolutions

---

### Terraform Setup

**Challenge:** Balancing realistic infra with assignment time limit.  
**Resolution:** Simulated EC2/RDS/ALB configurations using Terraform without actually applying it. Focused on code structure and reusability.

---

### CI/CD Pipeline

**Challenge:** Full end-to-end pipeline usually requires real deployments, secrets, and Docker registry access.  
**Resolution:** Mocked steps with clear placeholders and comments for where real logic goes (e.g., pushing to ECR, notifying via Slack).

---

### Monitoring & Logs

**Challenge:** Cannot set up real Prometheus/Grafana on a local machine easily.  
**Resolution:** Created sample configs and dummy logs. Included JSON for dashboards and explained future readiness.

---

### Secret Management

**Challenge:** Avoid exposing real tokens/credentials in public repo.  
**Resolution:** Used `.env` files locally and documented secret management options in README.

---

###  Documentation Scope

**Challenge:** Making sure the explanation is clear even though the app logic is skipped.  
**Resolution:** Focused on infrastructure, pipeline design, modularization, and included clear setup + decisions in README.md.

---

> Overall, every technical limitation was handled by a clean, professional workaround — simulating the intention clearly.
>  These trade-offs were made consciously to meet the 9–12 hr guideline and still reflect a realistic, maintainable DevOps solution.
