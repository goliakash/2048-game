🎮 2048 Game Deployment on Amazon EKS

An end-to-end DevOps project demonstrating how to containerize and deploy a web application on Amazon EKS (Elastic Kubernetes Service) using Docker, Kubernetes, and AWS services.

This project focuses on real-world cloud practices, including containerization, managed Kubernetes, cloud networking, and cost-aware infrastructure management.

🚀 Tech Stack

Docker – Containerization

Kubernetes – Orchestration

Amazon EKS – Managed Kubernetes

AWS ECR – Container Registry

AWS EC2 – Worker Nodes

AWS Load Balancer – External Access

Git & GitHub – Version Control

🏗️ Architecture Overview
User
 ↓
AWS Load Balancer
 ↓
Kubernetes Service (LoadBalancer)
 ↓
Kubernetes Pods
 ↓
Docker Container (2048 Game)

📁 Project Structure
.
├── Dockerfile
├── index.html
├── js/
├── style/
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── README.md
└── LICENSE.txt

🛠️ What I Did in This Project

Dockerized the 2048 web game using Nginx

Built and pushed the Docker image to AWS ECR

Created an Amazon EKS cluster using eksctl

Deployed the application using Kubernetes Deployment

Exposed the application using a Kubernetes LoadBalancer Service

Verified application availability via AWS public endpoint

Cleaned up AWS resources to avoid unnecessary cloud costs

🚀 Deployment Steps (High Level)
# Deploy application
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

# Check resources
kubectl get pods
kubectl get svc

🧪 Validation

Pods running successfully in EKS

Application accessible via AWS LoadBalancer

Multi-replica deployment for high availability

💡 Key Learnings

Hands-on experience with managed Kubernetes (EKS)

Deep understanding of IAM permission issues & debugging

Kubernetes deployments, services, and networking

Cost-aware cloud infrastructure management

Real-world DevOps troubleshooting (IAM, CloudFormation, EC2)

🧹 Cost Management

After successful deployment and testing, all AWS resources were deleted using eksctl to prevent unnecessary billing.

eksctl delete cluster --name game-2048-cluster --region ap-south-1

📌 Resume Highlight

Deployed a containerized 2048 web application on Amazon EKS using Docker and Kubernetes, implemented scalable deployments with LoadBalancer services, managed IAM permissions, and practiced cost-optimized cloud resource cleanup.

👨‍💻 Author

Akash
Aspiring DevOps Engineer | Cloud & devops Enthusiast
