# AWS Docker Terraform Portfolio Project

## 📌 Overview

This project demonstrates an end-to-end cloud deployment using AWS, Terraform, Docker, Git, and GitHub Actions.

The infrastructure is provisioned using Terraform, the application is containerized with Docker, deployed on an EC2 instance, and automatically updated through a CI/CD pipeline using GitHub Actions.

---

## 🚀 Features

- Infrastructure as Code (Terraform)
- Dockerized Portfolio Website
- AWS EC2 Deployment
- Git Version Control
- GitHub Actions CI/CD
- Automated Deployment on Git Push

---

## 🛠️ Technologies Used

- AWS EC2
- IAM
- Security Groups
- Terraform
- Docker
- Linux
- Git
- GitHub
- GitHub Actions

---

## 📂 Project Structure

aws-docker-terraform-project/
│
├── .github/
│   └── workflows/
│       ├── deploy.yml
│       └── deploy-app.yml
├── app/
│   ├── Dockerfile
│   ├── index.html
│   └── style.css
├── terraform/
│   ├── main.tf
│   ├── provider.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── versions.tf
├── screenshots/
├── .gitignore
└── README.md


##    Architecture
                Developer
                    │
                git push
                    │
                    ▼
          GitHub Repository
                    │
            GitHub Actions
                    │
                 SSH Login
                    ▼
             AWS EC2 Instance
                    │
          Docker Container
                    │
               Nginx Server
                    │
                    ▼
          Portfolio Website
