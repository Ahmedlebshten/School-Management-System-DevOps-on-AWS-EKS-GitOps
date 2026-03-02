# 🚀 School Management System – End-to-End DevOps Platform

## 📌 Overview

This project demonstrates a complete DevOps lifecycle implementation for a School Management System application deployed on AWS EKS using modern DevOps practices.

The platform includes:

- Infrastructure as Code (Terraform)
- Pipeline (GitHub Actions + AWS ECR)
- GitOps Continuous Deployment (ArgoCD)
- Kubernetes-native Monitoring Stack
- Production-oriented Kubernetes configuration
____

## 🏗 Architecture Diagram

![Architecture](./assets/architecture.jpeg)

____

## 🏗 Architecture Flow

#### 1️⃣ Infrastructure Repository (Jenkins + Terraform):

- Provisions AWS infrastructure using Terraform
- Creates VPC, IAM Roles, EKS Cluster, Node Groups
- Configures remote state (S3)
- Installs ArgoCD on EKS
- Bootstraps the Root Application

Infrastructure Lifecycle is isolated from application lifecycle.

🔗 Repository:
https://github.com/Ahmedlebshten/School_Management_System_Infra

____

#### 2️⃣ CI Repository (GitHub Actions):

Triggered on every push to the application repository:

- Builds Docker image
- Authenticates to AWS using OIDC (no static credentials)
- Pushes image to Amazon ECR
- Updates image tag in CD repository

Registry: Amazon ECR
```
731628759499.dkr.ecr.us-east-1.amazonaws.com/school-management-system:<build-number>
```
Images are built and pushed automatically by GitHub Actions using AWS OIDC authentication.

Flow:
```
Code Push
   ↓
GitHub Actions
   ↓
Build & Test
   ↓
Docker Build
   ↓
Trivy Scan
   ↓
Push to ECR
   ↓
Update CD Repo
   ↓
ArgoCD Sync
```
🔗 Repository:
https://github.com/Ahmedlebshten/School_Management_System
____

#### 3️⃣ GitOps CD Repository (ArgoCD):

- Watches CD repository
- Detects manifest changes
- Automatically syncs to EKS
- Applies self-healing & drift correction

Deploys:
- School Application
- MySQL (with PVC & StorageClass)
- Monitoring Stack (Helm-based)

🔗 Repository:
https://github.com/Ahmedlebshten/School_Management_System_CD
____

## 📊 Monitoring Stack
Deployed using Helm via GitOps model:

- Prometheus (Metrics)
- Grafana (Visualization)
- Loki (Logs)
- Promtail (Log shipping)

All running inside the cluster with Kubernetes-native configuration.
____

## 🛠 Technology Stack

- AWS (EKS, IAM, ECR, S3)
- Terraform
- Jenkins (Infrastructure pipeline)
- GitHub Actions (CI)
- Docker
- Kubernetes
- ArgoCD (GitOps CD)
- Helm
- Prometheus
- Grafana
- Loki
____

## 🎯 What This Project Demonstrates

- End-to-end DevOps lifecycle
- Infrastructure as Code (Terraform)
- CI/CD separation of concerns
- GitHub OIDC integration with AWS
- Private container registry (ECR)
- GitOps-based Kubernetes deployment
- Production-oriented Kubernetes configuration
- Persistent storage using EBS
- Monitoring & Observability implementation
	


## 📬 Reach Me

•  GitHub: [https://github.com/Ahmedlebshten]

•  LinkedIn: [https://www.linkedin.com/in/ahmedlebshten]

•  Email: [ahmedlebshtenlebshten@gmail.com]
   
⭐ Star this project if you find it useful! Production Ready - Fully Automated
