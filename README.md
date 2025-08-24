# Discover-Dollar_DevOps_Assignment--Ayush_Bhandari

## 📌 Project Overview

This project demonstrates the end-to-end setup of a **Full-Stack Application** (Frontend + Backend + Database) with **Docker, Docker Compose, Nginx, AWS EC2, and GitHub Actions**.  
The workflow covers local containerization, Nginx integration, cloud deployment, and CI/CD automation.

## 🚀 Steps Followed
### 1️⃣ Dockerization of Frontend & Backend
- Created separate **Dockerfiles** for:
  - **Backend** (`/backend/Dockerfile`)
  - **Frontend** (`/frontend/Dockerfile`)
- Wrote a **docker-compose.yaml** file to run both services together.
- Tested locally using:

      docker compose up

### 2️⃣ Adding Nginx for Frontend
* Modified the frontend Dockerfile to include Nginx as the web server.
* Configured Nginx to serve the built frontend files.
* Exposed port 80 for the frontend.
* Created a custom **nginx.conf** file in ./frontend to handle serving static files and routing.
* Tested locally by visiting:

      http://localhost:80
  
### 3️⃣ Deploying on AWS EC2
- Created an AWS EC2 instance (Ubuntu).
- Installed Docker and Docker Compose on the instance.
- Cloned the project repository to the server.
- Verified that the application runs on EC2 using:

      docker compose up


<img width="1907" height="1078" alt="5" src="https://github.com/user-attachments/assets/de6efb9c-908f-4a94-9a3d-9f0493933845" />


### 4️⃣ GitHub Actions CI/CD Pipeline
Created a GitHub Actions workflow (.github/workflows/ci.yml) with two jobs:
* Build & Push:
  - Builds Docker images for frontend & backend.
  - Pushes them to Docker Hub.
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/841d59da-9e6f-4802-b7af-39790b2e09e4" />

* Deploy on EC2:
  - Connects to AWS EC2 via SSH.
  - Pulls the latest Docker images.
  - Restarts containers using docker-compose up -d.


### 5️⃣ Automated Deployment Instructions
* After setup, deployment is fully automated:
  * Whenever code is pushed to the main branch:
      1. GitHub Actions builds Docker images.
      2. Pushes them to Docker Hub.
      3. Connects to EC2.
      4. Pulls the latest images.
      5. Runs the containers automatically.
  
No manual steps are needed after CI/CD setup ✅

---
## 🚀Working UI
<img width="1918" height="1078" alt="1" src="https://github.com/user-attachments/assets/ddd4de85-9b27-413b-a255-6b9c97ec9e49" />
<img width="1918" height="1078" alt="2" src="https://github.com/user-attachments/assets/67274922-854d-407f-b00d-3988fea133ea" />
<img width="1918" height="1078" alt="3" src="https://github.com/user-attachments/assets/1e5ce87c-d5e9-4757-9d85-42f807cbfd5a" />
<img width="1467" height="250" alt="4" src="https://github.com/user-attachments/assets/4a41c6ff-6fe0-4cf2-ab68-182450d134e6" />








