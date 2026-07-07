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

## ⚙️ Prerequisites

Before running this project, ensure you have:

- AWS Account
- Terraform Installed
- Docker Installed
- Git Installed
- AWS CLI Configured
- SSH Key Pair

## 🚀 Deployment Steps

1. Clone the repository

```bash
git clone https://github.com/mxdalll/aws-docker-terraform-project.git
```

2. Navigate to the Terraform directory

```bash
cd terraform
```

3. Initialize Terraform

```bash
terraform init
```

4. Validate the configuration

```bash
terraform validate
```

5. Create the infrastructure

```bash
terraform apply
```

6. Access the EC2 instance

```bash
ssh -i your-key.pem ec2-user@<EC2_PUBLIC_IP>
```

7. Build and run Docker

```bash
cd app
sudo docker build -t portfolio .
sudo docker run -d -p 80:80 --name portfolio-container portfolio
```
