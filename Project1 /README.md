# AWS EKS Production Deployment with ALB Ingress

Deploying a production-style Kubernetes application on Amazon Elastic Kubernetes Service (EKS) using AWS managed services.

---

## Project Overview

This project demonstrates how to deploy a containerized application on Amazon EKS using AWS best practices.

The infrastructure includes:

- Amazon EKS
- AWS Fargate
- VPC
- Public & Private Subnets
- IAM Roles for Service Accounts (IRSA)
- AWS Load Balancer Controller
- Application Load Balancer (ALB)
- Kubernetes Deployment
- Kubernetes Service
- Kubernetes Ingress

The application is deployed inside private subnets and exposed securely through an Application Load Balancer.

---

## Architecture

                   Internet
                       │
                       │
              Application Load Balancer
                       │
               AWS Load Balancer Controller
                       │
                  Kubernetes Ingress
                       │
                 Kubernetes Service
                       │
          ┌────────────┴────────────┐
          │                         │
      Pod Replica 1            Pod Replica 2
          │                         │
        Amazon EKS Cluster (Private Subnets)
                       │
                  AWS Fargate
                       │
                 Amazon VPC

---

## Technologies Used

- AWS EKS
- Kubernetes
- Docker
- Helm
- AWS CLI
- eksctl
- kubectl
- IAM
- OIDC
- IRSA
- ALB Ingress Controller
- AWS Fargate

---

## Project Workflow

1. Install AWS CLI, kubectl and eksctl
2. Create Amazon EKS Cluster
3. Configure kubeconfig
4. Create Fargate Profile
5. Deploy Application
6. Create Kubernetes Service
7. Configure IAM OIDC Provider
8. Install AWS Load Balancer Controller
9. Deploy Ingress Resource
10. Access Application using ALB DNS

---

## Deployment Steps

### Create Cluster

```bash
./eks/create-cluster.sh
```

### Update kubeconfig

```bash
./eks/update-kubeconfig.sh
```

### Deploy Application

```bash
kubectl apply -f manifests/
```

### Install AWS Load Balancer Controller

```bash
helm install aws-load-balancer-controller ...
```

---

## Result

- Amazon EKS Cluster Created
- Pods Running Successfully
- ALB Provisioned Automatically
- Application Accessible from Internet
- IAM Integrated using IRSA

---

## Learning Outcomes

- Amazon EKS Administration
- Kubernetes Networking
- ALB Ingress Controller
- AWS IAM Integration
- Helm Package Management
- Kubernetes Deployments
- Kubernetes Services
- Kubernetes Ingress
- Fargate Deployment

---

## Author

Neeraj Joshi

DevOps Engineer
