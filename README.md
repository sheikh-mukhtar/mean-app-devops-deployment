# 🚀 MEAN Stack Application Deployment using Docker, Nginx & GitHub Actions CI/CD

## 📌 Project Overview

This project demonstrates the complete containerization, orchestration, and deployment of a full-stack MEAN (MongoDB, Express.js, Angular, Node.js) application using industry-standard DevOps practices.

The application is deployed using Docker containers, managed via Docker Compose, served through an Nginx reverse proxy, and automated using GitHub Actions CI/CD pipeline with Docker Hub integration.

---

## 🏗️ Architecture

```text
User Browser
     │
     ▼
Nginx Reverse Proxy (Port 80)
     │
 ┌───────────────┐
 │               │
 ▼               ▼
Frontend       Backend
(Angular)     (Node.js)
                   │
                   ▼
                MongoDB
```

---

## 🛠️ Tech Stack

**Frontend**

* Angular 15
* Nginx

**Backend**

* Node.js
* Express.js

**Database**

* MongoDB

**DevOps Tools**

* Docker
* Docker Compose
* Docker Hub
* GitHub Actions
* Nginx Reverse Proxy

**Cloud Platform**

* AWS EC2 (Ubuntu)

---

## 📂 Project Structure

```
mean-app-devops-deployment/
│
├── frontend/
│   └── Dockerfile
│
├── backend/
│   └── Dockerfile
│
├── nginx/
│   └── default.conf
│
├── docker-compose.yml
│
├── .github/workflows/
│   └── cicd.yml
│
├── screenshots/
│   ├── app-running.png
│   └── cicd-success.png
│
└── README.md
```

---

## 🐳 Docker Setup

### Build and Run Application

```bash
docker compose up -d
```

### Stop Application

```bash
docker compose down
```

---

## 🌐 Nginx Reverse Proxy

Nginx is configured to route traffic:

* `/` → Frontend
* `/api` → Backend

Configuration file:

```
nginx/default.conf
```

Application accessible at:

```
http://localhost
```

or

```
http://<EC2-PUBLIC-IP>
```

---

## 🔄 CI/CD Pipeline (GitHub Actions)

The CI/CD pipeline automatically:

* Builds Docker images
* Pushes images to Docker Hub
* Enables automated deployment

Pipeline file:

```
.github/workflows/cicd.yml
```

Triggered on:

```
git push to main branch
```

---

## 📸 Screenshots

### Application Running

<img width="1916" height="917" alt="Screenshot 2026-02-24 110645" src="https://github.com/user-attachments/assets/5db0cd57-239c-474a-a0ba-33f30e34e928" />


---

### GitHub Actions CI/CD Pipeline Success

<img width="1916" height="917" alt="Screenshot 2026-02-24 110645" src="https://github.com/user-attachments/assets/6c2b984f-893b-40ee-96eb-3913656de345" />


---

## 📦 Docker Hub Images

Frontend Image:

```
mukhtarsheikh/mean-frontend:latest
```

Backend Image:

```
mukhtarsheikh/mean-backend:latest
```

---

## ☁️ Cloud Deployment Steps

1. Launch EC2 Ubuntu instance
2. Install Docker & Docker Compose
3. Clone GitHub repository

```bash
git clone https://github.com/sheikh-mukhtar/mean-app-devops-deployment.git
```

4. Run application

```bash
docker compose up -d
```

---

## 🧪 Testing

Frontend:

```
http://localhost
```

Backend:

```
http://localhost:8080
```

---

## ✅ Features Implemented

✔ Full-stack containerization
✔ Multi-container orchestration using Docker Compose
✔ MongoDB container integration
✔ Nginx reverse proxy setup
✔ Docker Hub image hosting
✔ GitHub Actions CI/CD pipeline
✔ AWS EC2 deployment ready

---

## 👨‍💻 Author

Mukhtar Sheikh

GitHub
https://github.com/sheikh-mukhtar

Docker Hub
https://hub.docker.com/u/mukhtarsheikh

LinkedIn
https://linkedin.com/in/mukhtarsheikh

---

## 🎯 Conclusion

This project demonstrates real-world DevOps workflow including containerization, CI/CD automation, reverse proxy configuration, and production deployment readiness.
