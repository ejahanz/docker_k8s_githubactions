🧱 Project Overview

📦 App: Simple Hello World Web App

Frontend: NGINX serving a static HTML page

Backend: Python Flask API responding with {"message": "Hello from backend"}

Database: (Optional — keep it simple to start)

# Docker + Kubernetes + GitHub Actions

A simple full-stack app to learn containers, orchestration, and CI/CD.

## Stack
- Python Flask Backend
- NGINX Frontend
- Kubernetes with Minikube
- GitHub Actions CI/CD

🗂️ Directory Structure

docker-k8s-actions-template/
├── backend/
│   ├── app.py
│   └── Dockerfile
├── frontend/
│   ├── index.html
│   └── Dockerfile
├── k8s/
│   ├── backend-deployment.yaml
│   ├── frontend-deployment.yaml
│   ├── service-backend.yaml
│   ├── service-frontend.yaml
│   └── ingress.yaml (optional)
├── .github/
│   └── workflows/
│       └── ci-cd.yaml
├── .dockerignore
├── .gitignore
└── README.md


## Run Locally
```bash
minikube start
kubectl apply -f k8s/
minikube service frontend-service

