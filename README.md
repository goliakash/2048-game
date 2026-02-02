# 🎮 2048 Game Deployment on Amazon EKS

This project demonstrates an end-to-end deployment of the **2048 web game** on **Amazon EKS** using **Docker, Kubernetes, and AWS services**.

## 🚀 Tech Stack
- Docker
- Kubernetes
- Amazon EKS
- AWS ECR
- AWS EC2
- AWS LoadBalancer

## 🏗 Architecture
User → AWS LoadBalancer → Kubernetes Service → Pods → Docker Container

## 📦 Project Structure
2048-eks-project/
├── 2048/
│ ├── Dockerfile
│ └── Game source code
├── k8s/
│ ├── deployment.yaml
│ └── service.yaml
└── README.md

## 🛠 Steps Performed
1. Dockerized the 2048 game
2. Pushed image to AWS ECR
3. Created EKS cluster using eksctl
4. Deployed application using Kubernetes Deployment
5. Exposed service using LoadBalancer

## 📌 How to Deploy
```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

