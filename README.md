# aws-secure-3-tier-architecture
Secure 3-tier architecture using AWS VPC, EC2, ALB, and RDS
# Secure 3-Tier Architecture on AWS

## Description
This project demonstrates a secure 3-tier architecture on AWS with proper network isolation and security best practices.

## Architecture Layers
- Web Tier: EC2 + Application Load Balancer (Public Subnets)
- App Tier: EC2 instances (Private Subnets)
- DB Tier: Amazon RDS (Private DB Subnets)

## Traffic Flow
Internet → ALB → Web Tier → App Tier → RDS

## Security Design
- Web tier accessible from internet via ALB
- Application tier accessible only from web tier
- Database accessible only from application tier
- No direct internet access to private tiers
