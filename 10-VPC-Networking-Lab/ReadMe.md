Cloud Fundamentals Lab - VPC Networking Lab

This project showcases the creation and configuration of a secure, scalable Virtual Private Cloud (VPC) environment using Amazon Web Services (AWS). It was completed as part of the Cloud Computing course at University Canada West (UCW) and simulates real-world enterprise network segmentation.

---

## 🌐 Project Overview

A **Virtual Private Cloud (VPC)** allows organizations to isolate and control their AWS infrastructure. This lab focuses on building a custom VPC setup from scratch to simulate a production-grade network with public-facing and private backend services.

---

![WhatsApp Image 2025-03-07 at 9 46 07 PM](https://github.com/user-attachments/assets/ed67f722-a5aa-4985-a829-a5c5b06a3def)

## 🧱 Architecture Breakdown

- **VPC Name:** `lab-vpc`
- **CIDR Block:** `10.0.0.0/16` (Allows creation of 65,536 IPs)
- **Subnets (in `us-east-1a`):**
  - `lab-subnet-public1-us-east-1a` → Hosts internet-facing components
  - `lab-subnet-private1-us-east-1a` → Hosts backend components (e.g., databases, internal services)

- **Route Tables:**
  - `lab-rtb-public` → Routes traffic to Internet Gateway for public subnet
  - `lab-rtb-private1-us-east-1a` → Routes outbound traffic to NAT Gateway

- **Gateways & Connectivity:**
  - `lab-igw` (Internet Gateway) → Enables outbound access for public subnet
  - `lab-nat-public1-us-east-1a` (NAT Gateway) → Allows private subnet to access the internet securely

- **Additional Settings:**
  - **DNS resolution & DNS hostnames**: Enabled for internal service discovery
  - **Network ACLs (NACLs)**: Custom ACLs applied to control inbound/outbound rules
  - **No public access** for private subnets

---

## 🎯 Objectives & Learning Outcomes

✅ Understand how AWS VPC provides isolation and segmentation for infrastructure  
✅ Learn how to route traffic via NAT and Internet Gateways  
✅ Practice real-world networking concepts like public/private subnet separation  
✅ Apply network-level security through ACLs and routing controls  
✅ Experience how DNS resolution and DHCP options affect VPC operations


---

## 🧠 Reflections

Building this project provided hands-on understanding of how **network segmentation** and **secure architecture** work in cloud environments. It helped reinforce the importance of:
- Isolating resources in private subnets
- Minimizing exposure via public IPs
- Routing wisely using NATs and IGWs
- Ensuring control over DNS and ACLs

---

## 🔐 Security Highlights

- ACLs created for added control (in addition to security groups)  
- Private subnet does not allow inbound traffic from the internet  
- DNS hostnames and resolution configured for service discovery  

---

## 📍 Tools & Services Used

- **Amazon VPC**  
- **Subnets**  
- **Route Tables**  
- **Internet Gateway (IGW)**  
- **NAT Gateway**  
- **Network ACLs**  
- **DNS, DHCP, CIDR**

---

## 📌 Status: ✅ Completed

This project demonstrates foundational skills needed to manage network infrastructure on AWS and lays the groundwork for more advanced architecture planning like VPC Peering, Transit Gateway, and Hybrid Cloud setups.
