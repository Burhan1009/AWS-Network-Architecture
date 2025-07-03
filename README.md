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

## 🌐 2️⃣ VPC and More
- In this option, your project goes beyond the VPC itself and also provisions other AWS resources (compute, storage, etc.)   that run inside the VPC..

### What’s included
- Everything in VPC Only, plus
- EC2 Instances (in public or private subnets)
- RDS/Databases (in private subnets)
- Application Load Balancers
- Auto Scaling Groups
- S3 Buckets
- IAM roles & policies

#### This option is good if
- You’re building a complete, end-to-end infrastructure ready to run workloads.
- You want to demonstrate full-stack AWS cloud deployment skills

## IPv4 CIDR Block | IPv4 CIDR | IPv6 CIDR block | Tenancy | Tags
![image](https://github.com/user-attachments/assets/f2cf3433-2801-422e-bb64-270ed7eb0e53)

### 📄 VPC Configuration: Description
This VPC is configured with a custom IPv4 CIDR block and an identifying name tag for easy management and visibility.
- ✅ The Name tag (TechD-VPC) is applied to the VPC resource to help distinguish it from other VPCs in the AWS account. Tags in AWS are key-value pairs you can use to organize, search, and track resources effectively.
- ✅ The IPv4 CIDR block is manually specified as 111.125.251.0/28.
- This defines the range of private IPv4 addresses available in this VPC.
- A /28 CIDR block supports 16 total IP addresses, out of which 11 are usable for resources like EC2 instances, NAT Gateway, etc.
- The small size (/28) suggests this VPC is designed for testing, demonstration, or small-scale workloads.
- ✅ The tenancy is set to default, which allows your EC2 instances and other resources to run on shared hardware.
- Hardware like Cisco Router , Juniper, Nokia, Cisco Switch etc
- ✅ A tag is added with key Name and value TechD-VPC to help identify the resource in the AWS console or CLI.
<hr/>

# Subnets Create 
Click on Create Subnet 
![image](https://github.com/user-attachments/assets/8fcfdbf6-b831-47d6-8766-5fa299517694)

## 🌩️ AWS VPC: TechD-VPC
This project creates a custom Virtual Private Cloud (VPC) in AWS with a clearly defined IPv4 CIDR block and name tag for easy identification.
It lays the foundation for deploying cloud resources in an isolated and secure environment.

```shell | Property           | Value                           |
|--------------------|---------------------------------|
| **VPC Name (tag)** | TechD-VPC                       |
| **VPC ID**         |          |
| **IPv4 CIDR Block**| 111.125.251.0/28               |
| **IPv6 CIDR Block**| Not configured                 |
| **Tenancy**        | Default (shared hardware)      |
```

![image](https://github.com/user-attachments/assets/c62ebf8c-4088-4389-967f-5ff6315dd197)

## Public Subnet

✅ Step 1: Name the Subnet Tag Key: Name | Tag Value: TechD-Pub-Subnet

✅ Step 2: Choose Availability Zone - Region: us-east-1 - AZ: us-east-1a

✅ Step 3: Select VPC CIDR block - VPC CIDR: 111.125.251.0/28

✅ Step 4: Define Subnet CIDR block - Subnet CIDR: 111.125.251.0/28 (16 IPs)

✅ Step 5: Add optional tags - Additional tags as needed

## Private Subnet 

Select VPC ID 

![image](https://github.com/user-attachments/assets/e009c36a-fed2-4375-a8df-e9fb890de6cd)

## Subnet Settings 
![image](https://github.com/user-attachments/assets/39f71dfb-5870-4ad6-8e42-fb10f3e0e1e5)

✅ Step 1: Name the Subnet : Tag Key: Name : Tag Value: TechD-Priv-Subnet

✅ Step 2: Choose Availability Zone : Region: us-east-1 : AZ: us-east-1a

✅ Step 3: Select VPC CIDR block : VPC CIDR: 111.125.251.0/28

✅ Step 4: Define Subnet CIDR block : Subnet CIDR: 111.125.252.0/28 (16 IPs)




