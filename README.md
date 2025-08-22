# eks-blueprint-terraform
Terraform configuration for provisioning and managing Amazon EKS clusters on AWS, following infrastructure-as-code best practices to ensure scalability, security, and consistency across environments.


# AWS CLI SETUP 
Link: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

🖥️ Linux
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

🍏 macOS
brew install awscli (Install with homebrew)

🪟 Windows
Download the installer: 👉 AWS CLI v2 MSI
Run the installer (Next → Next → Finish).

# Verify
aws --version
