# 🚀 End-to-End DevOps Automation Project

## 📌 Project Overview

This project demonstrates a complete **end-to-end DevOps automation workflow** by implementing Infrastructure as Code, configuration management, CI/CD automation, containerization, and Kubernetes deployment on AWS.

The project provisions AWS infrastructure using **Terraform**, configures servers automatically using **Ansible**, builds Docker images, and deploys applications to a Kubernetes cluster through a Jenkins CI/CD pipeline integrated with GitHub Webhooks.

---

# 🏗️ Architecture Overview

```
                         Developer
                             |
                             |
                         GitHub Repo
                             |
                             |
                    GitHub Webhook Trigger
                             |
                             v

                        Jenkins Server
                             |
             --------------------------------
             |                              |
             v                              v

       Build Docker Image             Push Image
             |                              |
             |                              |
             v                              v

        Docker Hub Registry
             
                             |
                             v

                    Kubernetes Cluster
                         (AWS EC2)

              ----------------------------
              |             |             |
              v             v             v

          Master Node    Worker Node   Worker Node


```

---

# 🛠️ Technologies Used

## Cloud Platform

- AWS EC2
- AWS VPC
- Security Groups
- Subnets


## Infrastructure as Code

- Terraform
- Terraform Modules


## Configuration Management

- Ansible


## CI/CD

- Jenkins
- GitHub Webhooks
- Jenkins Pipeline


## Containerization

- Docker
- Docker Hub


## Container Orchestration

- Kubernetes


## Operating System

- Linux Ubuntu


---

# 📂 Project Structure

```
.
│
├── main.tf
│
├── ansible-config-yml
│
├── Jenkinsfile
│
├── Dockerfile
│
├── deployment.yml
│
├── service.yml
│
├── script1.sh
├── script2.sh
├── script3.sh
│
├── index.html
│
└── images/

```

---

# ☁️ AWS Infrastructure Provisioning Using Terraform

Terraform is used to automatically create AWS infrastructure.

Infrastructure created:

- Custom VPC
- Public Subnets
- Internet Gateway
- Route Tables
- Security Groups
- EC2 Instances


## Infrastructure Layout

```
                 AWS VPC

                    |
        -------------------------
        |                       |
 Public Subnet 1        Public Subnet 2

        |                       |

 Kubernetes Master        Worker Nodes

        |
        |
 Jenkins Server

```

---

# 🏗️ Terraform Workflow

Initialize Terraform:

```bash
terraform init
```

Validate configuration:

```bash
terraform validate
```

Create execution plan:

```bash
terraform plan
```

Provision infrastructure:

```bash
terraform apply
```

Destroy infrastructure:

```bash
terraform destroy
```

---

# ⚙️ Server Configuration Using Ansible

After EC2 provisioning, Ansible automatically configures servers.

Configured components:

- Docker installation
- Kubernetes installation
- Required packages
- Node configuration


Workflow:

```
Terraform

    |
    |
Creates EC2 Instances

    |
    |
Ansible Playbook

    |
    |
Install Docker + Kubernetes

```

---

# 🐳 Docker Containerization

The application is containerized using Docker.

Dockerfile:

```
Application Source

        |
        |
    Docker Build

        |
        |
 Docker Image

        |
        |
 Docker Hub

```

Build Docker image:

```bash
docker build -t application-name .
```

Push image:

```bash
docker push username/application-name
```

---

# 🔄 Jenkins CI/CD Pipeline

Jenkins automates the complete application delivery process.

Pipeline stages:

```
GitHub Push

     |
     |
GitHub Webhook

     |
     |
 Jenkins Pipeline

     |
     |
Checkout Code

     |
     |
Build Docker Image

     |
     |
Push Image To Docker Hub

     |
     |
Deploy To Kubernetes

```

---

# 📜 Jenkins Pipeline Stages

Implemented stages:

### 1. Checkout

Pull application source code from GitHub.

---

### 2. Docker Build

Creates application container image.

Example:

```bash
docker build -t application .
```

---

### 3. Docker Push

Uploads image to Docker Hub.

---

### 4. Kubernetes Deployment

Deploys application using Kubernetes manifests.

---

# ☸️ Kubernetes Deployment

Kubernetes resources used:

## Deployment

`deployment.yml`

Responsible for:

- Creating pods
- Managing replicas
- Updating application versions


## Service

`service.yml`

Responsible for:

- Exposing application
- Internal/external communication


Deployment flow:

```
Docker Image

      |

 Kubernetes Deployment

      |

 Kubernetes Pods

      |

 Kubernetes Service

      |

 Users

```

---

# 🔔 GitHub Webhook Integration

GitHub webhook automatically triggers Jenkins whenever new code is pushed.

Flow:

```
Developer Push Code

        |

     GitHub

        |

 Webhook Trigger

        |

     Jenkins

        |

 Automated Deployment

```

---

# 🔐 Security Implementation

Implemented:

- AWS Security Groups
- SSH key authentication
- Restricted network access
- IAM permissions
- Secure Jenkins credentials


---

# 📊 DevOps Practices Demonstrated

✅ Infrastructure as Code  
✅ Automated server provisioning  
✅ Configuration management  
✅ CI/CD automation  
✅ Containerization  
✅ Kubernetes orchestration  
✅ GitOps workflow  
✅ Cloud infrastructure management  


---

# 📚 Learning Outcomes

Through this project, I gained hands-on experience with:

- Creating AWS infrastructure using Terraform modules
- Automating server configuration using Ansible
- Building CI/CD pipelines using Jenkins
- Containerizing applications with Docker
- Deploying applications on Kubernetes
- Implementing automated deployments using GitHub Webhooks


---

# 🔮 Future Improvements

Future enhancements:

- Deploy on AWS EKS
- Add Terraform remote backend with S3 and DynamoDB
- Add Prometheus and Grafana monitoring
- Implement Helm charts
- Add Kubernetes Ingress Controller
- Add SSL/TLS using Cert-Manager
- Implement ArgoCD GitOps deployment


---

# 👨‍💻 Author

**Abadur Rahaman Azmi**

DevOps Engineer

## Skills

AWS | Terraform | Ansible | Jenkins | Docker | Kubernetes | Linux | CI/CD | GitHub
