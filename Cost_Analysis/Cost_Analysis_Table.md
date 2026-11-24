# Task e: Cost Optimization Analysis Table

**Microservice:** Visitor Counter Web Application (Flask + Redis)  
**Target Platform:** Kubernetes & Hybrid Cloud Deployment  
**Student:** Prashant Yadav (`prashantyadavcs28-LAB`)  

---

## 1. Executive Summary Table

| Cost Category | Baseline Strategy (Annual) | Optimized Strategy (Annual) | Annual Net Savings | Percentage Reduction |
| :--- | :--- | :--- | :--- | :--- |
| **Compute Worker Nodes (EC2 / VM)** | \$1,681.92 | \$147.12 | \$1,534.80 | **-91.3%** |
| **Autoscaling Elasticity (HPA)** | \$990.00 | \$421.20 | \$568.80 | **-57.5%** |
| **Container Registry Storage (ECR)** | \$122.40 | \$14.40 | \$108.00 | **-88.2%** |
| **Data Transfer Egress (NAT Gateway)** | \$109.92 | \$13.44 | \$96.48 | **-87.8%** |
| **TOTAL ANNUAL EXPENDITURE** | **\$2,904.24** | **\$596.16** | **\$2,308.08** | **-79.5% Net Savings** |

---

## 2. Detailed Before vs. After Breakdown

| Technique | Metric | Before (Baseline) | After (Optimized) | Measured Savings / Improvement |
| :--- | :--- | :--- | :--- | :--- |
| **1. Image Size Reduction** | Base Docker Image | `python:3.11` Debian | `python:3.11-slim` Multi-stage | Compilers & build tools removed |
| 1. Image Size Reduction | Container Image Size | **1,018 MB (1.02 GB)** | **124 MB** | **-87.8% (894 MB eliminated)** |
| 1. Image Size Reduction | Cold-Start Pull Latency | 16.3 seconds | 1.9 seconds | **88.3% faster pod startup** |
| 1. Image Size Reduction | Known Vulnerabilities (CVEs)| 184 CVEs | 24 CVEs | **-86.9% security attack surface** |
| 1. Image Size Reduction | Monthly Registry Storage | \$1.02 / month | \$0.12 / month | **-88.2% storage cost** |
| **2. Workload Right-Sizing** | Web Pod CPU / RAM Request | 1000m / 1024 MiB | 100m / 128 MiB | **10x CPU, 8x RAM reduction** |
| 2. Workload Right-Sizing | Total Cluster Reserved vCPU | 2.50 vCPU | 0.25 vCPU | **90.0% vCPU capacity reclaimed** |
| 2. Workload Right-Sizing | Pod Packing Density (2-vCPU node)| 2 pods / node | 18 pods / node | **9x container density increase** |
| 2. Workload Right-Sizing | Required Cloud Compute Node | 2x `m5.large` (\$140.16/mo) | 1x `t4g.small` (\$12.26/mo) | **91.3% compute cost reduction** |
| **3. Autoscaling Elasticity** | Average Daily Pod Count | 6.00 pods (static 24/7) | 2.55 effective pods (HPA) | **-57.5% compute load** |
| 3. Autoscaling Elasticity | Monthly Compute Cost | \$82.50 / month | \$35.10 / month | **-\$47.40 / mo (-\$568.80 / yr)** |
