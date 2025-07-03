![image](https://github.com/user-attachments/assets/cde7c484-9962-4217-915b-699e812e1845)

# AWS-Network-Architecture
This project showcases a cloud infrastructure with public subnets for frontend/admin, private subnets for databases (MySQL, Oracle, DocumentDB), and a separate VPC for testing (Ansible, RDP). It uses NAT Gateway and VPC Peering for secure communication

## 🧰 Technologies & Services

- **AWS VPC**
- **Subnets (Public & Private)**
- **Internet Gateway**
- **NAT Gateway**
- **Route Tables**
- **Security Groups & NACLs**
- Terraform / AWS CLI (if applicable)

## 🚀 Features

✅ Create a VPC with a customizable CIDR block  
✅ Provision public & private subnets in multiple AZs  
✅ Set up Internet Gateway & NAT Gateway for internet access  
✅ Configure route tables & security groups  
✅ Easy-to-follow steps or IaC (Infrastructure as Code)<br/>
✅ Setup VPC Peering

## VPC Settings : Resources to create 
![image](https://github.com/user-attachments/assets/50d4c07b-deea-40c5-97e0-99967f3a71d3)

## 🌐 1️⃣ VPC Only
- In this option, your project focuses only on building the networking layer (VPC).
  You create and configure just the VPC and its networking components.

### What’s included
- VPC
- Subnets (public & private)
- Internet Gateway
- NAT Gateway
- Route Tables
- Security Groups
- Network ACLs

#### This option is good if
- You just need to prepare a secure, scalable network foundation.
- Application, EC2 instances, databases, and other services will be deployed later by someone else
- You want to showcase expertise in AWS networking only.
