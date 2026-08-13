# Compliance Documentation 

 

 

## Overview 

 

 

This folder contains compliance, governance and incident response documentation produced for the MediCore Health Systems secure cloud infrastructure project. 

 

 

The documents within this folder demonstrate how the deployed AWS environment supports legal, regulatory and security obligations relating to healthcare data processing. 

 

 

The documentation aligns with: 

 

 

- UK GDPR 

 

- Data Protection Act 2018 

 

- NHS Data Security and Protection Toolkit (DSPT) 

 

- NCSC Incident Management Guidance 

 

- ISO 27001 security principles 

 

 

--- 

 

 

## Contents 

 

 

### MediCore-IRP-v1.md 

 

 

The primary Incident Response Plan (IRP) for MediCore Health Systems. 

 

 

The document outlines: 

 

 

- Preparation activities 

 

- Incident identification procedures 

 

- Containment actions 

 

- Eradication procedures 

 

- Recovery procedures 

 

- Lessons learned process 

 

 

--- 

 

 

## Incident Response Scope 

 

 

The Incident Response Plan applies to the deployed AWS environment including: 

 

 

- Bastion Host 

 

- EC2 Application Server 

 

- Amazon RDS Database 

 

- Amazon S3 Storage 

 

- AWS CloudWatch Monitoring 

 

- Auto Scaling Group 

 

- Load Balancer 

 

 

--- 

 

 

## Monitoring Controls 

 

 

The Incident Response Plan references the following CloudWatch alerts: 

 

 

1. MC-CPU-High 

 

2. MC-DiskRead-High 

 

3. MC-DiskWrite-High 

 

4. MC-NetworkIn-High 

 

5. MC-NetworkOut-High 

 

 

These alerts support the early detection of security incidents and operational issues. 

 

 

--- 

 

 

## Supporting Compliance Requirements 

 

 

The documentation supports: 

 

 

### UK GDPR Article 32 

 

 

Security of processing through: 

 

 

- Network segmentation 

 

- Encryption 

 

- Monitoring and alerting 

 

- Backup and recovery controls 

 

 

### UK GDPR Article 33 

 

 

Data breach notification procedures including: 

 

 

- Incident detection 

 

- Escalation process 

 

- ICO notification requirements within 72 hours 

 

 

### UK GDPR Article 9 

 

 

Protection of special category health data processed within the MediCore environment. 

 

 

--- 

 

 

## Evidence 

 

 

Supporting screenshots for compliance and monitoring controls are located within the repository screenshots folder. 

 

 

Monitoring evidence used within the Incident Response Plan is available within the analysis folder. 

 

 

 
