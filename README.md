# Cloud DevOps Multi-Container Platform

Production microservices infrastructure hosting a Cloud & DevOps engineering portfolio and a containerized cloud storage service with automated CI/CD and custom DNS routing.

## 🌐 Live Deployments
- **Portfolio Frontend**: [https://raheemcloud.tech](https://raheemcloud.tech)
- **CloudDrive Backend**: [https://drive.raheemcloud.tech](https://drive.raheemcloud.tech)

## 🏗️ Architecture & Tech Stack
- **Frontend**: Lightweight, high-performance static portfolio.
- **Backend**: Python (Flask, Gunicorn, SQLite, Boto3) running in Docker.
- **Reverse Proxy & Routing**: Nginx container handling request proxying, header forwarding, and SSL/TLS termination.
- **Orchestration**: Docker Compose bridging services over an isolated internal network (`devops-network`).
- **CI/CD Pipeline**: GitHub Actions testing Compose configurations and container builds on every push to `main`.
- **DNS & CDN**: Namecheap DNS managing apex (`@`) and subdomain (`drive`) routing with automated Let's Encrypt certificates.