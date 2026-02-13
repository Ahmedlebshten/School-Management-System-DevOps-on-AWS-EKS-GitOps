# 🚀 School Management System – End-to-End DevOps Platform

📌 Overview

This project demonstrates a complete DevOps lifecycle implementation for a School Management System application deployed on AWS EKS using modern DevOps practices.

The platform includes:

	•	Infrastructure as Code (Terraform)
	•	CI Pipeline (Docker Build & Push)
	•	GitOps Continuous Deployment (ArgoCD)
	•	Kubernetes-native Monitoring Stack

⸻

🏗 Architecture Flow

1️⃣ Infrastructure Pipeline
	•	Provisions AWS infrastructure using Terraform
	•	Creates EKS cluster
	•	Bootstraps ArgoCD
	•	Deploys Root Application

2️⃣ CI Pipeline
	•	Builds Docker image
	•	Pushes image to DockerHub
	•	Updates image tag

3️⃣ GitOps CD (ArgoCD)
	•	Watches CD repository
	•	Automatically syncs changes to EKS
	•	Deploys application and monitoring stack

⸻

📦 Repositories Structure

🏗 Infrastructure Repository

Terraform + Jenkins

Handles:
	•	AWS provisioning
	•	EKS cluster creation
	•	ArgoCD installation
	•	Root Application creation

🔗 Repo Link:
[https://github.com/YOUR_USERNAME/School_Management_System_Infra(https://github.com/Ahmedlebshten/School_Management_System_Infra)

⸻

🔁 CI Repository

Docker Build & Image Push

Handles:
	•	Application build
	•	Docker image creation
	•	Push to DockerHub

🔗 Repo Link:
[https://github.com/YOUR_USERNAME/School_Management_System_CI](https://github.com/Ahmedlebshten/School_Management_System)

⸻

🚀 CD Repository

ArgoCD GitOps Deployment

Handles:
	•	Kubernetes manifests
	•	Monitoring stack
	•	ArgoCD Applications
	•	Automated sync & self-heal

🔗 Repo Link:
[https://github.com/YOUR_USERNAME/School_Management_System_CD](https://github.com/Ahmedlebshten/School_Management_System_CD)

⸻

🐳 Container Image

| Image | Registry | Latest Tag |
|-------|----------|------------|
| school_management_system | Docker Hub | v4 |

🔗 Docker Hub:
[https://hub.docker.com/r/ahmedlebshten/school_management_system](https://hub.docker.com/repository/docker/ahmedlebshten/school_management_system/general)

⸻

📊 Monitoring Stack
	•	Prometheus (Metrics)
	•	Grafana (Visualization)
	•	Loki (Logs)
	•	Promtail (Log shipping)

Deployed via GitOps model.

⸻

🛠 Technologies Used
	•	AWS
	•	EKS
	•	Terraform
	•	Jenkins
	•	Docker
	•	ArgoCD
	•	Kubernetes
	•	Prometheus
	•	Grafana
	•	Loki

⸻

🎯 What This Project Demonstrates
	•	Real-world DevOps architecture
	•	Infrastructure as Code
	•	GitOps workflow
	•	CI/CD separation of concerns
	•	Kubernetes-native deployment
	•	Monitoring & observability setup
	
⸻

📬 Contact

   •  GitHub: [https://github.com/Ahmedlebshten]
   
   •  LinkedIn: [https://www.linkedin.com/in/ahmedlebshten]
   
   •  Email: [ahmedlebshtenlebshten@gmail.com]
   
⭐ Star this project if you find it useful! DevSecOps Pipeline - Production Ready - Fully Automated
