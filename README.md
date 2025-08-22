# eks-blueprint-terraform
Terraform configuration for provisioning and managing Amazon EKS clusters on AWS, following infrastructure-as-code best practices to ensure scalability, security, and consistency across environments.

# 📋 Prerequisites
 1.Terraform >= 1.3.0
 2.AWS CLI v2
 3.An AWS account with credentials configured: aws configure / aws configure sso
 
# aws sso login : 
aws sso login --profile dev-sso
aws sso login --profile stage-sso
aws sso login --profile prod-sso

# ⚡ Quick Start
Clone this repo: 
git clone https://github.com/maheshdash5/eks-blueprint-terraform
cd eks-blueprint-terraform

# Initialize Terraform:
terraform init

# Plan the changes:
terraform plan

# Apply to create the EKS cluster:
terraform apply -auto-approve

# 🔑 Configure kubectl
aws eks --region us-east-1 update-kubeconfig --name my-eks-cluster

# Test connectivity:
kubectl get nodes

# 🧹 Cleanup
To destroy all resources:
terraform destroy -auto-approve


# AWS CLI SETUP : https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

# 🖥️ Linux
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

# 🍏 macOS
brew install awscli (Install with homebrew)

# 🪟 Windows
Download the installer: 👉 AWS CLI v2 MSI
Run the installer (Next → Next → Finish).

# Verify
aws --version


# Kubectl CLI SETUP :
# 🖥️ Linux
curl -LO "https://dl.k8s.io/release/$(curl -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/

# 🍏 macOS
Option 1: Homebrew (easiest)
brew install kubectl

# 🪟 Windows
Using Chocolatey
choco install kubernetes-cli

# Verify
kubectl version --client

📚 References

Terraform Documentation: https://developer.hashicorp.com/terraform/docs
Amazon EKS Documentation: https://docs.aws.amazon.com/eks/index.html
kubectl Cheat Sheet: https://kubernetes.io/docs/reference/kubectl/cheatsheet/
