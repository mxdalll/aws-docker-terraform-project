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

## 🔄 CI/CD Workflow

The project uses GitHub Actions to automate deployments.

Workflow:

Developer
    │
git push
    │
    ▼
GitHub Repository
    │
GitHub Actions
    │
SSH into EC2
    │
git pull
    │
Docker Build
    │
Restart Container
    │
Updated Portfolio Website

## 📸 Screenshots

- GitHub Repository
- GitHub Actions
- EC2 Instance
- Security Group
- Terraform Apply
- Docker Container
- Portfolio Website

## 🐞 Troubleshooting

During this project, the following issues were resolved:

- Terraform resource reference errors
- AMI lookup issues
- Free Tier instance compatibility
- SSH key pair configuration
- SCP permission issues
- Git large file errors (.terraform)
- Git remote conflicts
- GitHub Actions formatting errors
- Docker daemon issues
- EC2 Security Group configuration
- CI/CD deployment pipeline configuration

## 📈 Future Improvements

- Deploy using AWS ECS
- Add Application Load Balancer
- Use Terraform Remote State
- Configure a Custom Domain
- Enable HTTPS with ACM
- Add Monitoring using CloudWatch

## 📸 Screenshots

### GitHub Repository

![GitHub Repository](screenshots/01-github-repo.png)

### GitHub Actions

![GitHub Actions](screenshots/02-github-actions.png)

### AWS EC2 Instance

![EC2](screenshots/03-ec2.png)

### Portfolio Website

![Website](screenshots/04-website.png)



<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/7a5c11fa-7a78-4515-b0c9-df25700cae8b" />
