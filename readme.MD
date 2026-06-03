<div align="center">

# 🚀 Docker-Roboshop

### Containerized Microservices Application using Docker & Docker Compose

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge\&logo=amazonaws\&logoColor=FF9900)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge\&logo=linux\&logoColor=black)

**A production-ready implementation of the Roboshop Microservices Application using Docker, Docker Compose, and DevOps best practices.**

</div>

---

## 📖 Overview

Docker-Roboshop demonstrates how to containerize and orchestrate a complete microservices-based e-commerce application using Docker and Docker Compose.

### 🎯 Key Objectives

* Containerize microservices using Docker
* Implement multi-stage builds
* Run containers as non-root users
* Configure service-to-service networking
* Manage application dependencies
* Deploy a complete microservices stack

---

## 🏗️ Architecture

### Application Services

| Service   | Technology     |
| --------- | -------------- |
| Frontend  | Nginx          |
| User      | Node.js        |
| Catalogue | Node.js        |
| Cart      | Node.js        |
| Shipping  | Java           |
| Payment   | Python         |
| MongoDB   | Database       |
| MySQL     | Database       |
| Redis     | Cache          |
| RabbitMQ  | Message Broker |

---

## 📂 Repository Structure

```text
Docker-Roboshop/
├── frontend/
├── user/
├── catalogue/
├── cart/
├── shipping/
├── payment/
├── mongodb/
├── mysql/
├── docker-compose.yaml
└── README.md
```

---

## ✨ Features

* 🐳 Multi-stage Docker Builds
* 🔒 Non-root User Containers
* ⚡ Lightweight Runtime Images
* 🌐 Docker Networking
* 📦 Docker Compose Orchestration
* 🛡️ Security Best Practices
* 🚀 Production Ready Deployment

---

## 📋 Prerequisites

* Docker 20+
* Docker Compose
* Git

---

## 📥 Clone Repository

```bash
git clone https://github.com/Anil-Kumar-Akula/Docker-Roboshop.git

cd Docker-Roboshop
```

---

## 🔨 Build Images

Build all services:

```bash
docker compose build
```

Build an individual service:

```bash
docker build -t frontend ./frontend
docker build -t user ./user
docker build -t catalogue ./catalogue
docker build -t cart ./cart
docker build -t shipping ./shipping
docker build -t payment ./payment
```

---

## 🚀 Run the Application

Start all services:

```bash
docker compose up -d
```

Check running containers:

```bash
docker ps
```

View logs:

```bash
docker compose logs -f
```

Stop all services:

```bash
docker compose down
```

---

## 🔐 Docker Best Practices

### Multi-Stage Builds

Used to reduce image size and improve security by separating build and runtime environments.

### Non-Root User

```dockerfile
RUN addgroup -S roboshop && \
    adduser -S roboshop -G roboshop

USER roboshop
```

### Optimized Images

* Alpine-based Images
* Reduced Attack Surface
* Faster Deployments

---

## 🌐 Networking

Docker Compose automatically creates a dedicated network allowing services to communicate using service names.

Example:

```text
cart:8080
catalogue:8080
user:8080
shipping:8080
mysql
mongodb
redis
rabbitmq
```

---

## 🛠️ Useful Commands

```bash
docker ps
docker logs <container-name>
docker exec -it <container-name> sh
docker network ls
docker network inspect <network-name>
```

---

## 🎓 Learning Outcomes

This project demonstrates:

* Docker Fundamentals
* Dockerfile Best Practices
* Multi-Stage Builds
* Container Security
* Docker Networking
* Docker Compose
* Microservices Deployment

---

## 👨‍💻 Author

### Anil Kumar Akula


