
# AWS MLOps & Cloud Engineering Portfolio

An end-to-end collection of production-grade Machine Learning Operations (MLOps) and Cloud DevOps projects built on **Amazon Web Services (AWS)**. 

This repository demonstrates how machine learning workflows integrate with modern DevOps practices—including Infrastructure as Code (IaC), containerization, event-driven CI/CD pipelines, automated retraining, and model drift monitoring.

---

## Architecture & Engineering Principles
Every project in this repository follows core production standards:
* **Infrastructure as Code (IaC):** All cloud resources (S3, ECR, IAM, SageMaker, Lambda) are provisioned declaratively rather than manually via the console.
* **Reproducibility:** Training and inference environments are containerized with Docker and versioned in Amazon ECR.
* **Event-Driven Automation:** Pipelines trigger automatically on code commits (`git push`) or new data arrivals in Amazon S3.
* **Cost & Security Hygiene:** Least-privilege IAM roles, automated resource teardown scripts, and serverless inference endpoints to minimize idle cloud spend.

---

## Projects Index

| # | Project Name | Use Case | Core AWS & DevOps Stack | Status |
| :--- | :--- | :--- | :--- | :--- |
| **01** | [`01-aws-sagemaker-churn-pipeline`](./01-aws-sagemaker-churn-pipeline) | Event-driven customer churn training & serverless API deployment | SageMaker, S3, ECR, Lambda, EventBridge, Docker, GitHub Actions, Terraform | 🚧 In Progress |
| **02** | `02-eks-mlflow-fraud-detection` | Distributed model tracking & Kubernetes serving with canary rollouts | Amazon EKS, MLflow, Docker, Prometheus, Grafana | 📋 Planned |
| **03** | `03-bedrock-rag-llmops-pipeline` | Automated document ingestion, evaluation & guardrails for GenAI | Amazon Bedrock, OpenSearch, Step Functions, CloudWatch | 📋 Planned |

---

## Tech Stack Overview

* **Cloud Platform:** Amazon Web Services (SageMaker, S3, ECR, Lambda, EventBridge, API Gateway, IAM, CloudWatch)
* **Infrastructure as Code:** Terraform, AWS CloudFormation
* **CI/CD & Automation:** GitHub Actions, AWS CodePipeline
* **Containers & Orchestration:** Docker, Amazon ECS / EKS
* **ML & Data Frameworks:** Python, Scikit-Learn, Pandas, MLflow

---

## Repository Structure

Each project is isolated in its own directory with independent dependencies, infrastructure definitions, and scoped CI/CD workflows:

```text
aws-mlops-portfolio/
├── README.md                            # Portfolio overview and project index
├── .gitignore                           # Global ignores for Python, Terraform, and AWS credentials
├── 01-aws-sagemaker-churn-pipeline/     # Project 1: Automated SageMaker training & inference
│   ├── .github/workflows/               # Path-scoped CI/CD pipelines
│   ├── infrastructure/                  # IaC templates (S3, ECR, IAM, EventBridge)
│   ├── docker/                          # Training & serving Dockerfiles
│   ├── src/                             # Preprocessing, training, and inference code
│   └── tests/                           # Unit and data validation tests
└── ...                                  # Future MLOps projects
```

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com<your-username>/aws-mlops-portfolio.git
   cd aws-mlops-portfolio
   ```
2. **Navigate to a specific project:**
   Each subfolder contains its own `README.md` with step-by-step deployment, testing, and teardown instructions.
3. **Prerequisites:**
   * An active AWS Account with configured CLI credentials (`aws configure`)
   * Docker Desktop installed locally
   * Terraform or AWS CLI v2
