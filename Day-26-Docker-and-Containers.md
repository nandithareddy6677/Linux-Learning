# Day 26: Docker & Containers

> Understanding Docker, Containers, Images, Containerization, Docker architecture, and why containers are widely used in cloud computing.

---

# 🎯 Learning Objectives

- Understand Containers.
- Learn Docker Architecture.
- Understand Images.
- Learn Docker Commands.
- Explore Container Benefits.
- Prepare for Cloud & DevOps interviews.

---

# 📖 Introduction

Traditional applications run directly on an operating system.

Containers package applications together with their dependencies, ensuring they run consistently across different environments.

Docker is the most popular platform for containerization.

---

# 🐳 What is Docker?

Docker is an open-source platform used to build, package, and run applications inside lightweight containers.

---

# What is a Container?

A Container is an isolated environment containing:

- Application
- Libraries
- Dependencies
- Configuration Files

Containers share the host operating system kernel.

---

# Docker Architecture

```
Developer

↓

Docker Client

↓

Docker Engine

↓

Docker Images

↓

Docker Containers
```

---

# Docker Image

A Docker Image is a read-only template used to create containers.

Examples:

- Ubuntu Image
- Nginx Image
- MySQL Image

---

# Docker Container

A running instance of a Docker Image.

One image can create multiple containers.

---

# Common Docker Commands

Check version:

```bash
docker --version
```

List containers:

```bash
docker ps
```

List all containers:

```bash
docker ps -a
```

List images:

```bash
docker images
```

Pull an image:

```bash
docker pull ubuntu
```

Run container:

```bash
docker run ubuntu
```

Stop container:

```bash
docker stop <container-id>
```

Remove container:

```bash
docker rm <container-id>
```

---

# Benefits of Docker

- Fast Deployment
- Portability
- Lightweight
- Scalability
- Easy Rollback
- Consistent Environment

---

# Docker in Cloud Computing

Docker is widely used in:

- AWS ECS
- AWS EKS
- Azure AKS
- Google Kubernetes Engine

---

# 🌍 Real-Life Example

A developer creates a web application.

Instead of installing dependencies on every server, they package everything into a Docker container.

The same container runs consistently on development, testing, and production systems.

---

# 💡 Best Practices

- Use official Docker images.
- Keep images updated.
- Remove unused containers.
- Minimize image size.
- Scan images for vulnerabilities.

---

# 📌 Key Takeaways

- Docker simplifies application deployment.
- Containers are lightweight.
- Images are templates.
- Containers improve portability.
- Docker is widely used in cloud platforms.

---

# ❓ Interview Questions

### 1. What is Docker?

A platform used to build and run containerized applications.

### 2. What is a Docker Image?

A template used to create containers.

### 3. What is a Docker Container?

A running instance of a Docker Image.

### 4. Why are containers preferred over traditional deployment?

They are lightweight, portable, and consistent.

### 5. Name two cloud services that support Docker.

- AWS ECS
- Azure AKS

---

# 📝 Summary

Today I learned about Docker, Containers, Images, Docker architecture, and how containerization simplifies application deployment across cloud environments.
