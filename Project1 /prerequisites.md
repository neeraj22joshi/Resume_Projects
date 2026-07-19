# Prerequisites

Before deploying the application, ensure the following tools are installed and configured on your local machine:

| Tool | Description |
|------|-------------|
| **kubectl** | Kubernetes command-line tool used to deploy, manage, and troubleshoot resources in an Amazon EKS cluster. |
| **eksctl** | Official command-line utility for creating, managing, and deleting Amazon EKS clusters with minimal configuration. |
| **AWS CLI** | AWS Command Line Interface used to configure AWS credentials and interact with AWS services such as EKS, IAM, VPC, and EC2. |
| **Helm** | Kubernetes package manager used to install and manage applications and add-ons, such as the AWS Load Balancer Controller. |

## Verify Installation

```bash
kubectl version --client

eksctl version

aws --version

helm version
```

## AWS Configuration

Configure your AWS credentials before creating the EKS cluster:

```bash
aws configure
```

Provide the following details when prompted:

- AWS Access Key ID
- AWS Secret Access Key
- Default Region (e.g., `ap-south-1`)
- Default Output Format (`json`)
