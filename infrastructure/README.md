# Infrastructure Configuration 

 

 

## Overview 

 

 

This folder contains the infrastructure configuration and supporting evidence used to deploy the MediCore Health Systems AWS environment. 

 

 

The environment was designed using a three-tier architecture to support security, scalability and compliance requirements for healthcare data processing. 

 

 

--- 

 

 

## Infrastructure Components 

 

 

### Virtual Private Cloud (VPC) 

 

 

A dedicated VPC was created to isolate MediCore resources from other AWS environments. 

 

 

### Public Subnet 

 

 

Contains the Bastion Host which acts as the sole administrative entry point into the environment. 

 

 

Purpose: 

 

- Secure administration 

 

- Controlled SSH access 

 

- Reduced attack surface 

 

 

### Private Subnet 

 

 

Hosts the application server. 

 

 

Purpose: 

 

- Application processing 

 

- No direct administrative internet access 

 

- Additional network protection 

 

 

### Restricted Subnet 

 

 

Contains the Amazon RDS database. 

 

 

Purpose: 

 

- Patient data storage 

 

- Segregated from internet-facing resources 

 

- Database access restricted to approved application resources 

 

 

--- 

 

 

## Security Controls 

 

 

### Security Groups 

 

 

Security Groups were implemented according to least-privilege principles. 

 

 

Rules included: 

 

 

- SSH access restricted to approved source IP addresses 

 

- Application ports restricted to authorised traffic 

 

- Database access limited to application resources 

 

- Deny-by-default approach implemented 

 

 

### Encryption 

 

 

Encryption was enabled to protect patient information. 

 

 

Implemented controls: 

 

 

- Amazon RDS encryption at rest 

 

- S3 encryption at rest 

 

- TLS encryption for data in transit 

 

 

### Identity and Access Management 

 

 

IAM roles were configured to support role-based access control. 

 

 

Roles implemented: 

 

 

- Clinical Read Only 

 

- Clinical Write 

 

- Database Administrator 

 

- Monitoring Role 

 

- Backup Operator 

 

 

--- 

 

 

## Monitoring 

 

 

AWS CloudWatch was configured to monitor infrastructure performance and security events. 

 

 

Alerts configured: 

 

 

- CPU Utilisation High 

 

- Disk Read High 

 

- Disk Write High 

 

- Network In High 

 

- Network Out High 

 

 

These alerts support proactive monitoring and incident detection. 

 

 

--- 

 

 

## High Availability 

 

 

To improve resilience, the environment includes: 

 

 

- Auto Scaling configuration 

 

- Load Balancer 

 

- Multiple Availability Zones 

 

 

These controls minimise service disruption and improve availability. 

 

 

--- 

 

 

## Evidence 

 

 

Supporting evidence can be found within the /screenshots directory. 

 

 

Evidence includes: 

 

 

- VPC configuration 

 

- Subnet architecture 

 

- Security Groups 

 

- IAM Roles 

 

- CloudWatch Alerts 

 

- Auto Scaling configuration 

 

- Load Balancer configuration 

 

- RDS configuration 

 

 
