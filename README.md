

# Terraform Automated AWS Infrastructure

This project demonstrates the automated provisioning of a production-ready AWS infrastructure using **Terraform**, organized with reusable modules for **VPC** and **EKS**. The setup is designed for scalability, security, and high availability, following best practices for cloud infrastructure automation.

---

## Project Structure

```
.
├── main.tf                  # Root Terraform configuration
├── variables.tf             # Root-level variables
├── outputs.tf               # Root-level outputs
├── backend/                 # Backend state configuration
│   ├── main.tf
│   ├── outputs.tf
│   ├── terraform.tfstate
│   └── terraform.tfstate.backup
├── modules/
│   ├── vpc/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── eks/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
```

---

## Modules

### **VPC Module**

* Creates a **custom VPC** with **public and private subnets** across multiple Availability Zones.
* Configures **Internet Gateway** and **NAT Gateways** for secure internet access.
* Sets up **route tables, NACLs, and Security Groups** for network security and controlled traffic flow.

### **EKS Module**

* Deploys an **Amazon EKS cluster** with **Fargate or managed worker nodes**.
* Configures **node groups, IAM roles, and security policies** for the cluster.
* Optionally integrates **ALB Ingress Controller** for scalable, public-facing services.
* Supports automated deployment using **Terraform variables** for flexible configurations.

---

## Features

* Modular design for **reusability and maintainability**.
* Multi-AZ deployment for **high availability**.
* Secure network setup with **private subnets and bastion access**.
* Scalable Kubernetes workloads on **AWS EKS**.
* Backend state management for **team collaboration and state locking** (via S3 + DynamoDB).

---

## Usage

1. **Clone the repository**

```bash
git clone https://github.com/sohitji725/terraform-automated-aws-infrastructure.git
cd terraform-automated-aws-infrastructure
```

2. **Initialize Terraform**

```bash
terraform init
```

3. **Plan the deployment**

```bash
terraform plan
```

4. **Apply the configuration**

```bash
terraform apply
```

5. **Destroy resources (if needed)**

```bash
terraform destroy
```

---

## Learnings & Key Takeaways

* Hands-on experience in **modular Terraform architecture**.
* Implemented **VPC networking and security best practices**.
* Deployed **scalable Kubernetes clusters on EKS**.
* Gained knowledge of **Terraform backend configuration and state management**.
* Learned to **automate infrastructure provisioning** for production-ready environments.

---


# Terraform Automated AWS Infrastructure

This project demonstrates the automated provisioning of a production-ready AWS infrastructure using **Terraform**, organized with reusable modules for **VPC** and **EKS**. The setup is designed for scalability, security, and high availability, following best practices for cloud infrastructure automation.

---

## Project Structure

```
.
├── main.tf                  # Root Terraform configuration
├── variables.tf             # Root-level variables
├── outputs.tf               # Root-level outputs
├── backend/                 # Backend state configuration
│   ├── main.tf
│   ├── outputs.tf
│   ├── terraform.tfstate
│   └── terraform.tfstate.backup
├── modules/
│   ├── vpc/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── eks/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
```

---

## Modules

### **VPC Module**

* Creates a **custom VPC** with **public and private subnets** across multiple Availability Zones.
* Configures **Internet Gateway** and **NAT Gateways** for secure internet access.
* Sets up **route tables, NACLs, and Security Groups** for network security and controlled traffic flow.

### **EKS Module**

* Deploys an **Amazon EKS cluster** with **Fargate or managed worker nodes**.
* Configures **node groups, IAM roles, and security policies** for the cluster.
* Optionally integrates **ALB Ingress Controller** for scalable, public-facing services.
* Supports automated deployment using **Terraform variables** for flexible configurations.

---

## Features

* Modular design for **reusability and maintainability**.
* Multi-AZ deployment for **high availability**.
* Secure network setup with **private subnets and bastion access**.
* Scalable Kubernetes workloads on **AWS EKS**.
* Backend state management for **team collaboration and state locking** (via S3 + DynamoDB).

---

## Usage

1. **Clone the repository**

```bash
git clone https://github.com/sohitji725/terraform-automated-aws-infrastructure.git
cd terraform-automated-aws-infrastructure
```

2. **Initialize Terraform**

```bash
terraform init
```

3. **Plan the deployment**

```bash
terraform plan
```

4. **Apply the configuration**

```bash
terraform apply
```

5. **Destroy resources (if needed)**

```bash
terraform destroy
```

---

## Learnings & Key Takeaways

* Hands-on experience in **modular Terraform architecture**.
* Implemented **VPC networking and security best practices**.
* Deployed **scalable Kubernetes clusters on EKS**.
* Gained knowledge of **Terraform backend configuration and state management**.
* Learned to **automate infrastructure provisioning** for production-ready environments.

---
