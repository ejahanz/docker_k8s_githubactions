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

docker-k8s-actions-template/<br>
├── backend/<br>
│   ├── app.py<br>
│   └── Dockerfile<br>
├── frontend/<br>
│   ├── index.html<br>
│   └── Dockerfile<br>
├── k8s/<br>
│   ├── backend-deployment.yaml<br>
│   ├── frontend-deployment.yaml<br>
│   ├── service-backend.yaml<br>
│   ├── service-frontend.yaml<br>
│   └── ingress.yaml (optional)<br>
├── .github/<br>
│   └── workflows/<br>
│       └── ci-cd.yaml<br>
├── .dockerignore<br>
├── .gitignore<br>
└── README.md


## Run Locally
```bash
minikube start
kubectl apply -f k8s/
minikube service frontend-service

