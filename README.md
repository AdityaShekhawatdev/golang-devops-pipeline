# 🚀 Golang Cloud-Native DevOps Pipeline

A professional, end-to-end containerized microservice project built to demonstrate modern DevOps practices using **Golang**, **Docker**, **Kubernetes (Minikube)**, and **GitHub Actions**.

## 🛠️ Tech Stack
- **Language:** Go (Golang) - Lightweight & High Performance
- **Containerization:** Docker (Multi-stage builds for minimal image size)
- **Orchestration:** Kubernetes (Deployments & NodePort Services)
- **Environment:** WSL (Windows Subsystem for Linux)

---

## 📂 Project Structure
```text
golang-devops-pipeline/
├── main.go            # Go REST API source code
├── go.mod             # Go module dependencies
├── Dockerfile         # Multi-stage optimized Docker build
├── app-deploy.yaml    # Kubernetes Deployment & Service manifests
├── .gitignore         # Git ignore rules
└── README.md          # Project documentation
```

# 🚀 Getting Started Locally

## 1. Build & Run via Docker

Bash

### Build the Docker image
docker build -t golang-devops-app .

### Run the container
docker run -d -p 8080:8080 --name go-app-container golang-devops-app

## 2. Deploy to Kubernetes (Minikube)
Bash
#### Load image into minikube
minikube image load golang-devops-app

### Apply Kubernetes manifests
kubectl apply -f app-deploy.yaml

### Access the app via port-forwarding
kubectl port-forward svc/golang-app-service 8080:80