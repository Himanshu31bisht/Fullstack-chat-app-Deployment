# 🚀 Fullstack Chat App – Docker & Kubernetes Deployment

This repository contains the **deployment setup** for the **Fullstack Chat Application**, containerized with **Docker** and orchestrated using **Kubernetes (Minikube)**.

---

## 🧱 Tech Stack
- **Frontend:** React.js (served via Nginx)  
- **Backend:** Node.js & Express  
- **Database:** MongoDB (Docker container)  
- **Containerization:** Docker, Docker Compose  
- **Orchestration:** Kubernetes (Minikube)  

---

## 🐳 Docker Setup

### 1. Build and Run Containers
```bash
docker-compose up --build
2. Stop Containers
bash
Copy code
docker-compose down
☸️ Kubernetes Deployment (Minikube)
1. Start Minikube
bash
Copy code
minikube start
2. Apply Kubernetes Manifests
bash
Copy code
kubectl apply -f k8s/
3. Verify Resources
bash
Copy code
kubectl get pods
kubectl get services
4. Access the Application
bash
Copy code
minikube service frontend-service
📝 Setup .env File:
Navigate to the backend directory:

bash
Copy code
cd backend
Create a .env file and add the following content (modify the values as needed):

env
Copy code
MONGODB_URI=mongodb://mongoadmin:secret@mongodb:27017/dbname?authSource=admin
JWT_SECRET=your_jwt_secret_key
PORT=5001
Note: Replace your_jwt_secret_key with a strong secret key of your choice.

📦 Folder Structure
bash
Copy code
Fullstack-chat-app-Deployment/
│
├── backend/
│   ├── Dockerfile
│   ├── .env
│   └── ...
│
├── frontend/
│   ├── Dockerfile
│   └── ...
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
└── docker-compose.yml
🧩 Key Highlights
Deployed on Minikube using Ingress, Services, and Persistent Volumes

Dockerized all components (Frontend, Backend, MongoDB)

Scalable, containerized, and ready for production-level orchestration