# AWS Shared Storage Architecture Using Amazon FSx for Windows File Server

## Project Overview

This project demonstrates the implementation of a centralized shared storage architecture on AWS using Amazon FSx for Windows File Server.

The goal of this project was to allow multiple EC2 Windows servers to access the same shared file storage securely.

---

## Architecture

The architecture consists of:

- Active Directory Domain Controller
- Server-1 (EC2) in Availability Zone: ap-south-1a
- Server-2 (EC2) in Availability Zone: ap-south-1b
- Amazon FSx for Windows File Server as centralized shared storage
- Security Groups for access control

Architecture Flow:

Users/Servers  
↓  
EC2 Windows Servers  
↓  
Amazon FSx for Windows File Server  
↓  
Shared File Storage

---

## AWS Services Used

### Amazon EC2
- Created Windows EC2 instances
- Used servers for testing shared storage access

### Amazon FSx for Windows File Server
- Created managed Windows file storage
- Provided centralized shared file access

### Active Directory
- Used for authentication and domain management

### Security Groups
- Configured network access between EC2 instances and FSx

### Amazon VPC
- Used AWS networking environment for resource deployment

---

## Implementation Steps

1. Created EC2 Windows instances.
2. Configured Active Directory environment.
3. Created Amazon FSx for Windows File Server.
4. Configured security group rules for communication.
5. Connected EC2 servers with FSx storage.
6. Accessed shared files from multiple servers.

---

## Outcome

Successfully accessed the same shared files from multiple servers using Amazon FSx as centralized storage.

This project helped me understand:

- AWS storage services
- Windows file sharing
- SMB protocol
- Security Group configuration
- Cloud infrastructure design

---

## Security Note

For learning and testing purposes, broader inbound access was allowed during configuration.

In a production environment, Security Groups should follow the principle of least privilege and allow only required ports, such as:

- SMB (445)
- Active Directory required ports

---

## Screenshots

(Add your screenshots here)

Example:

![FSx Configuration](screenshots/fsx.png)

![EC2 Server Connection](screenshots/ec2.png)

---

## Project Demo

Video demonstration:
(Add your LinkedIn/YouTube/Drive link here)

---

## Skills Learned

- AWS Cloud Computing
- Amazon EC2
- Amazon FSx
- Active Directory
- Windows Server
- Security Groups
- SMB Protocol
- Cloud Storage Architecture