# EKS Terraform Infrastructure

Terraform module for provisioning a production-ready Amazon EKS cluster with VPC, managed node groups, and IAM configurations.

## Infrastructure Components

- VPC with multi-AZ public subnets
- EKS Control Plane (Kubernetes 1.29)
- Managed Node Group with auto-scaling
- IAM roles with least-privilege policies

## Prerequisites

- AWS CLI configured
- Terraform >= 1.0
- kubectl

## Deployment

```bash
terraform init
terraform plan
terraform apply
Connect to Cluster
bash
aws eks update-kubeconfig --region us-east-1 --name my-eks-cluster
kubectl get nodes
Configuration
Variable	Default	Description
region	us-east-1	AWS region
cluster_name	my-eks-cluster	EKS cluster name
cluster_version	1.29	Kubernetes version
Cleanup
bash
terraform destroy
Author
Sagar - GitHub

License
MIT
git branch -M main
git remote add origin git@github.com:sagar3414/eks-terraform.git
git push -u origin main
