# MediCore Health Systems - Secure Clinical Cloud Infrastructure 

 

 

## Overview 

 

 

This repository contains the implementation, configuration evidence, security documentation and supporting artefacts for the DTS202 Data Governance and Compliance assignment. 

 

 

The project was developed for the fictional organisation MediCore Health Systems, a healthcare provider responsible for managing approximately 140,000 patient records. The objective was to design and implement a secure, scalable and compliant cloud infrastructure capable of supporting NHS Digital Security and Protection Toolkit (DSPT) requirements and UK GDPR obligations. 

 

 

The solution was deployed using Amazon Web Services (AWS) and incorporates security, monitoring, scalability, containerisation and compliance controls. 

 

 

--- 

 

 

# Architecture Overview 

 

 

The infrastructure follows a three-tier architecture: 

 

 

### Public Subnet 

 

- Bastion Host 

 

- Sole internet-facing entry point 

 

- Restricted SSH access 

 

 

### Private Subnet 

 

- Application Server (EC2) 

 

- Hosts MediCore web application 

 

- No direct administrative access from the internet 

 

 

### Restricted Subnet 

 

- Amazon RDS Database 

 

- Encrypted at rest using AES-256 

 

- Accessible only from the application server 

 

 

### Supporting Services 

 

- Amazon S3 

 

- AWS IAM 

 

- AWS CloudWatch 

 

- Auto Scaling Group 

 

- Load Balancer 

 

- Docker 

 

- Kubernetes 

 

 

This architecture supports the principles of least privilege, defence in depth and network segmentation. 

 

 

--- 

 

 

# Security Controls Implemented 

 

 

## Network Security 

 

 

- Security Groups configured with deny-by-default principles 

 

- SSH restricted to the Bastion Host 

 

- Database accessible only from authorised application resources 

 

- Segmented subnet architecture 

 

 

## Identity and Access Management 

 

 

The following IAM roles were configured: 

 

 

1. Clinical Read Only 

 

2. Clinical Write 

 

3. Database Administrator 

 

4. Monitoring Role 

 

5. Backup Operator 

 

 

Each role follows least-privilege principles. 

 

 

## Encryption 

 

 

### Data at Rest 

 

 

- Amazon RDS encryption enabled 

 

- Amazon S3 encryption enabled 

 

- AWS managed encryption controls utilised 

 

 

### Data in Transit 

 

 

- HTTPS/TLS configured for secure communications 

 

 

## Monitoring 

 

 

AWS CloudWatch monitoring was configured including: 

 

 

- CPU Utilisation High 

 

- Disk Read High 

 

- Disk Write High 

 

- Network In High 

 

- Network Out High 

 

 

CloudWatch alarms support proactive security monitoring and incident detection. 

 

 

--- 

 

 

# Scalability and High Availability 

 

 

The deployment incorporates: 

 

 

- Auto Scaling configuration 

 

- Load Balancer 

 

- Multiple Availability Zones 

 

- Health checks 

 

- Fault tolerance controls 

 

 

These measures improve resilience and availability for healthcare workloads. 

 

 

--- 

 

 

# Containerisation 

 

 

Docker was used to containerise the application. 

 

 

Security measures included: 

 

 

- Non-root container execution 

 

- Read-only file system 

 

- Resource limits 

 

- Secure Docker configuration 

 

 

Supporting Kubernetes deployment files are stored in the /kubernetes directory. 

 

 

--- 

 

 

# Data Visualisation and Analysis 

 

 

CloudWatch monitoring data was exported and analysed. 

 

 

Visualisations produced: 

 

 

1. EC2 CPU Utilisation Over Time 

 

2. Network Inbound Traffic Monitoring 

 

 

These visualisations are stored within the /analysis directory and support risk analysis activities documented within the assignment report. 

 

 

--- 

 

 

# Repository Structure 

 

 
