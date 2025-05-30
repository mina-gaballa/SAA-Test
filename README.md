# SAA-Test

## AWS Solutions Architect Associate (SAA) - Course Repository

This repository contains resources, notes, and code examples for the "SAA - AWS 2: Becoming a Solutions Architect" course by Manara.


## Course Overview

This course prepares you for the AWS Solutions Architect Associate certification (SAA-C03). It covers AWS core services, solution design patterns, best practices, and hands-on labs.

**Topics include:**
- AWS Core Services (EC2, S3, RDS, Lambda, etc.)
- Networking and Security
- High Availability and Fault Tolerance
- Cost Optimization
- Monitoring and Logging

## Repository Structure

- `/notes/` — Course notes and summaries
- `/labs/` — Hands-on lab exercises and solutions
- `/diagrams/` — Architecture diagrams and reference images
- `/scripts/` — Useful scripts for AWS automation

> You can update this section to reflect your actual directory structure.

## Architecture Diagram

The following diagram illustrates a typical AWS multi-tier web application architecture. It demonstrates a secure, highly available, and scalable deployment using several AWS services and best practices:

![Architecture Diagram](image1)

**Description:**

- **Route 53** manages DNS traffic and directs user requests.
- **VPC** spans two Availability Zones for high availability and fault tolerance.
  - **Public Subnet** contains a NAT Gateway and Bastion host for secure admin access.
  - **Private Subnets** are used for the web, application, and database tiers.
- **Internet Gateway** provides public internet access to the load balancer and Bastion host.
- **Load Balancers:**
  - Internet-facing load balancer distributes traffic to web-tier EC2 instances.
  - Internal load balancer routes traffic from the web-tier to the app-tier EC2 instances.
- **Security Groups** protect each tier (web, app, database), controlling traffic flow.
- **EC2 Instances** run in both the web and app tiers, distributed across private subnets.
- **Amazon RDS (MySQL)** provides the database layer with a primary instance and read replica, both in private subnets.
- **Bastion Host** allows secure SSH access, and the NAT Gateway enables outbound internet access for instances in private subnets.

This architecture supports a scalable, secure, and highly available web application, following AWS best practices for network security, redundancy, and separation of concerns.

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/mina-gaballa/SAA-Test.git
   ```
2. Navigate to the desired folder (e.g., `notes` or `labs`).
3. Follow instructions in each folder's README or documentation.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request to suggest improvements or add new content.

## License

This project is licensed under the MIT License.

---

**Maintainer:** [mina-gaballa](https://github.com/mina-gaballa)
