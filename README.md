# Terraform Automated AWS Infrastructure

This project demonstrates the automated provisioning of a production-ready AWS infrastructure using **Terraform**, organized with reusable modules for **VPC** and **EKS**. The setup is designed for scalability, security, and high availability, following best practices for cloud infrastructure automation.

---

## Project Structure

.
├── main.tf # Root Terraform configuration
├── variables.tf # Root-level variables
├── outputs.tf # Root-level outputs
├── backend/ # Backend state configuration
│ ├── main.tf
│ ├── outputs.tf
│ ├── terraform.tfstate
│ └── terraform.tfstate.backup
├── modules/
│ ├── vpc/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── outputs.tf
│ └── eks/
│ ├── main.tf
│ ├── variables.tf
│ └── outputs.tf

yaml
Copy code

---

## Modules

### VPC Module
- Creates a **custom VPC** with public and private subnets across multiple Availability Zones.  
- Configures **Internet Gateway** and **NAT Gateways** for secure internet access.  
- Sets up **route tables, NACLs, and Security Groups** for network security and controlled traffic flow.  

### EKS Module
- Deploys an **Amazon EKS cluster** with Fargate or managed worker nodes.  
- Configures **node groups, IAM roles, and security policies** for the cluster.  
- Optionally integrates **ALB Ingress Controller** for scalable, public-facing services.  
- Supports automated deployment using **Terraform variables** for flexible configurations.  

---

## Features
- Modular design for **reusability and maintainability**  
- Multi-AZ deployment for **high availability**  
- Secure network setup with **private subnets and bastion access**  
- Scalable Kubernetes workloads on **AWS EKS**  
- Backend state management for **team collaboration and state locking** (via S3 + DynamoDB)  

---

## Usage

**Clone the repository**
```bash
git clone https://github.com/sohitji725/terraform-automated-aws-infrastructure.git
cd terraform-automated-aws-infrastructure
Initialize Terraform

bash
Copy code
terraform init
Plan the deployment

bash
Copy code
terraform plan
Apply the configuration

bash
Copy code
terraform apply
Destroy resources (if needed)

bash
Copy code
terraform destroy
Learnings & Key Takeaways
Hands-on experience in modular Terraform architecture

Implemented VPC networking and security best practices

Deployed scalable Kubernetes clusters on EKS

Gained knowledge of Terraform backend configuration and state management

Learned to automate infrastructure provisioning for production-ready environments

pgsql
Copy code

This version is fully Markdown-compliant and ready to paste directly into a `README.md` on GitHub. It preserves **code blocks, headings, lists, and formatting** for readability.  

If you want, I can also **shorten it for a portfolio-friendly README** so recruiters can quickly u
