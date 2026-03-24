# Cloud-Native To-Do Application Deployment (Docker + Kubernetes + AWS EKS)

## 📌 Project Overview
This project demonstrates the end-to-end deployment of a cloud-native To-Do web application using Flask and MongoDB, containerized with Docker, and deployed using Kubernetes both locally (Minikube) and on the cloud (AWS EKS).

The goal of this project was to understand how modern applications are built, deployed, scaled, and monitored in a production-like environment.

---

## 🧱 Tech Stack
- Backend: Flask (Python)
- Database: MongoDB
- Containerization: Docker
- Orchestration: Kubernetes
- Local Cluster: Minikube
- Cloud Platform: AWS EKS
- Monitoring: Kubernetes Probes (Liveness and Readiness)
- Alerting (Optional): Prometheus and Slack

---

## ⚙️ Project Architecture
The system consists of:
- Flask application container
- MongoDB container for persistent storage
- Docker Hub for image storage
- Kubernetes for orchestration
- AWS EKS for cloud deployment
- Prometheus for monitoring and alerting

---

## 🚀 Features Implemented

### Containerization
- Created Docker images for Flask app and MongoDB
- Used docker-compose for local testing

### Kubernetes Deployment (Minikube)
- Created pods for Flask and MongoDB
- Defined deployments and services
- Exposed application via Kubernetes service

### AWS EKS Deployment
- Set up EKS cluster
- Configured kubectl for remote access
- Deployed application to cloud environment
- Verified external accessibility

### Deployments and ReplicaSets
- Configured desired replica count
- Tested self-healing by deleting pods
- Performed scaling (up and down replicas)

### Rolling Updates
- Implemented rolling update strategy
- Updated Docker image version
- Monitored rollout without downtime

### Health Monitoring
- Configured:
  - Liveness probes (check if app is alive)
  - Readiness probes (check if app is ready)
- Tested failure scenarios and recovery

### Alerting (Extra)
- Integrated Prometheus for monitoring
- Configured alert triggers
- Sent alerts via Slack

---

## 🛠️ Setup Instructions

### 1. Clone Repository
```bash
git clone <your-repo-link>
cd <project-folder>
```

### 2. Build Docker Image
```bash
docker build -t flask-app .
```

### 3. Run Locally (Docker Compose)
```bash
docker-compose up
```

### 4. Run on Minikube
```bash
minikube start
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 5. Deploy on AWS EKS
- Create EKS cluster
- Configure kubectl
- Apply Kubernetes configuration files

---

## 📊 Key Learnings
- Understanding containerization using Docker
- Deploying applications using Kubernetes
- Managing replicas and scaling
- Implementing zero-downtime deployments
- Monitoring and maintaining application health
- Deploying production-grade systems on AWS

---

## 👩‍💻 Contributors
- You
- Your Teammate

---

## 📌 Conclusion
This project provided hands-on experience in building and deploying a scalable, reliable, and production-ready application using modern cloud-native technologies. It helped bridge the gap between development and real-world deployment practices.
