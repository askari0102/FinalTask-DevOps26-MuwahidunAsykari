# 🚀 End-to-End DevOps Lifecycle Implementation

**Final Task DumbWays DevOps Batch 26 - Muwahidun Asykari**

## 📖 Summary
This repository contains the documentation and infrastructure code for deploying a microservices application (Frontend React.js & Backend Golang). 

The infrastructure is provisioned on **AWS** using a combination of public and private subnets. A Gateway server acts as both a reverse proxy and a **Bastion Host** in the public subnet to securely access the application servers located in the private subnet. A **NAT Gateway** is implemented to handle outbound internet traffic for the private instances. 

The project uses **Terraform** for Infrastructure as Code (IaC) and **Ansible** for configuration management. The deployment lifecycle is automated using **GitLab CI/CD** pipelines for the Staging environment, and a **GitOps** workflow using **FluxCD** and **Kubernetes (k3s)** for the Production environment. The ecosystem is monitored using Prometheus and Grafana.

---

## 🏗️ Architecture Topology
<img width="1412" height="672" alt="server_topology_transparent (1)" src="https://github.com/user-attachments/assets/199847d7-d08f-4ca1-a92e-75a4cc53fb6f" />

---

## 🛠️ Tech Stack & Tools Used

| Category | Tools |
| :--- | :--- |
| **Cloud Provider** | AWS (EC2, VPC, NAT Gateway, IAM, Elastic IP) |
| **Infrastructure as Code** | Terraform |
| **Config Management** | Ansible, Ansible Vault |
| **Containers & Orchestrator**| Docker, Kubernetes (k3s) |
| **CI/CD & GitOps** | GitLab CI/CD, FluxCD |
| **Code Quality** | SonarQube |
| **Observability** | Prometheus, Grafana, cAdvisor, Node Exporter |
| **Networking & Security** | NGINX, Cloudflare DNS, Let's Encrypt, UFW |
| **Scripting & OS** | Bash/Shell, Ubuntu 22.04 LTS |

---

## 📂 Project Navigation & Documentation

Below is the step-by-step documentation of the entire DevOps lifecycle. Click on each section to view the detailed implementation guides, scripts, and configurations.

### 1 - [Provisioning](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/1%20-%20Provisioning)
> AWS environment setup and Terraform IaC implementation for VPC, Public/Private Subnets, NAT Gateway, and EC2 instances.

### 2 - [Repository](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/2%20-%20Repository)
> GitLab private repository setup, branch protection, code migration, and GitOps environment preparation.

### 3 - [Servers](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/3%20-%20Servers)
> Automated server configurations using Ansible, including SSH port modification (Port 6969), UFW Firewall rules, and user management across the bastion and private servers.

### 4 - [Container Registry](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/4%20-%20Container%20Registry)
> Deployment of a Private Docker Registry integrated with an Nginx reverse proxy and basic authentication.

### 5 - [Deployment](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/5%20-%20Deployment)
> Multi-stage Docker builds, environment variable injection, and Staging server deployment using Docker Compose and PostgreSQL.

### 6 - [CI/CD](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/6%20-%20CI%20CD)
> GitLab CI/CD pipelines setup featuring SonarQube code quality checks, automated Docker image builds, and deployment triggers for both Staging (via SSH) and Production (via GitOps).

### 7 - [Monitoring](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/7%20-%20Monitoring)
> Prometheus and Grafana setup with custom PromQL dashboards for VM and container metrics, integrated with Telegram bot alerts.

### 8 - [Web Server](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/8%20-%20Web%20Server)
> Centralized Gateway server configuration using Nginx as a reverse proxy and bastion host, along with automated Let's Encrypt Wildcard SSL certificates via the Cloudflare API.

### 9 - [Kubernetes](https://github.com/askari0102/FinalTask-DevOps26-MuwahidunAsykari/tree/main/9%20-%20Kubernetes)
> Production k3s cluster setup, Nginx Ingress Controller deployment, and continuous deployment automation using FluxCD.
