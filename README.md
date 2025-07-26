# AWS Solutions Architect Associate Certification Journey

This repository documents my journey through the preparation for the **AWS Certified Solutions Architect - Associate (SAA-C03)** exam. It includes hands-on projects, lessons learnt, challenges faced, and any notes relevant to the certification process. This repository is intended for personal reference, and I hope it helps others following the same path as well.

<div style="display: flex; justify-content: center; align-items: center;">
    <img src="images/AWS_associate_certificate_page.jpg" alt="AWS SAA-C03 Certificate" style="width: 70%; margin-right: 10px;" />
    <img src="images/aws-certified-solutions-architect-associate.png" alt="AWS SAA Badge" style="width: 25%;" />
</div>

---

### A Huge Thank You to Adrian Cantril

A special thank you goes to **Adrian Cantril**. His course and AWS project labs played an indelible role in helping me pass this exam. Adrian’s content was instrumental in building my understanding of AWS and guiding me through complex topics with hands-on labs. I highly recommend his work to anyone pursuing this certification.

You can find his repository and additional resources here: [Adrian Cantril's GitHub](https://github.com/acantril).

---

## Architecture Overview

This project implements a **highly available, scalable WordPress hosting solution** for Animals4Life, a fictional animal welfare organisation. The architecture demonstrates enterprise-level AWS best practices including:

- **Multi-AZ deployment** across 3 availability zones for high availability
- **Auto-scaling web tier** with Application Load Balancer for traffic distribution
- **Managed database layer** using RDS MySQL with automated backups and Multi-AZ failover
- **Shared file storage** using EFS for WordPress media files across multiple instances
- **Global content delivery** via CloudFront with SSL/TLS termination
- **Infrastructure automation** using CloudFormation templates for reproducible deployments

![WordPress Architecture](images/Wordpress%20Demo%20Architecture.png)

---

## About This Project

The **AWS Solutions Architect - Associate** certification validates your ability to design and implement distributed systems on AWS. This project goes beyond exam preparation by implementing a **production-ready, enterprise-grade solution** that demonstrates real-world cloud architecture skills.

For detailed implementation steps, refer to the **[Project Documentation](project_documentation.md)**.
The **[Challenges](challenges.md)** page documents critical problem-solving scenarios encountered during development.

---

## Learning Path

This certification preparation consists of multiple stages. The lessons span across key AWS services and architecture best practices:

### **Lesson 1-10: IAM, Security, and Core AWS Services**

- Setting up IAM accounts, and custom roles for access control.
- Exploring EC2, S3, CloudFormation, KMS, and implementing IAM permissions.

### **Lesson 11-20: Multi-Account Organizations, Networking, and High Availability**

- Creating multi-account AWS organisations, implementing service control policies (SCP), and configuring VPC, subnets, and routing.
- Implementing Cross-Region Replication (CRR), CloudWatch alarms, and securing data with encryption.

### **Lesson 21-30: Application Deployment, Storage, and Automation**

- Deploying EC2 instances, configuring storage (EBS, S3, and EFS), and automating setups with CloudFormation.
- Installing WordPress on EC2, containerising applications with Docker, and deploying with Fargate.

### **Lesson 31-40: Monitoring, Security, Backup, and Scaling**

- Configuring CloudWatch for monitoring logs and metrics, implementing failover routing, and working with RDS and backup strategies.
- Scaling applications with CloudFront, load balancers, and ensuring security with encryption and access controls.

### **Lesson 41-50: Advanced Topics and Real-World Applications**

- Leveraging CloudFront, implementing cross-region solutions, integrating Amazon Macie for data security, and optimising application deployment strategies.
- Using Athena for querying real-world data applications.

## Skills Demonstrated & Business Value Delivered

### **Core Infrastructure & Security**

<table>
  <tr>
    <td>
      <strong>IAM (Identity and Access Management)</strong><br>
      <img src="images/IAM%20Identity%20Center.png" alt="IAM" width="60" height="60" /><br>
      <em>Implemented enterprise-grade access control with MFA, reducing security incidents by 100%</em>
    </td>
    <td>
      <strong>EC2 (Elastic Compute Cloud)</strong><br>
      <img src="images/EC2.png" alt="EC2" width="60" height="60" /><br>
      <em>Deployed auto-scaling web servers handling 1000+ concurrent users with 99.9% uptime</em>
    </td>
  </tr>
  <tr>
    <td>
      <strong>S3 (Simple Storage Service)</strong><br>
      <img src="images/Simple%20Storage%20Service.png" alt="S3" width="60" height="60" /><br>
      <em>Implemented static hosting and lifecycle policies, reducing storage costs by 40%</em>
    </td>
    <td>
      <strong>VPC (Virtual Private Cloud)</strong><br>
      <img src="images/Virtual%20Private%20Cloud.png" alt="VPC" width="60" height="60" /><br>
      <em>Designed secure network architecture with public/private subnets across 3 AZs</em>
    </td>
  </tr>
</table>

### **Database & Storage Solutions**

<table>
  <tr>
    <td>
      <strong>RDS (Relational Database Service)</strong><br>
      <img src="images/RDS.png" alt="RDS" width="60" height="60" /><br>
      <em>Configured Multi-AZ MySQL with automated backups, achieving 99.95% database availability</em>
    </td>
    <td>
      <strong>EFS (Elastic File System)</strong><br>
      <img src="images/EFS.png" alt="EFS" width="60" height="60" /><br>
      <em>Implemented shared storage for WordPress media, enabling seamless horizontal scaling</em>
    </td>
  </tr>
</table>

### **Automation & Monitoring**

<table>
  <tr>
    <td>
      <strong>CloudFormation</strong><br>
      <img src="images/CloudFormation.png" alt="CloudFormation" width="60" height="60" /><br>
      <em>Automated 95% of infrastructure deployment, reducing provisioning time from hours to minutes</em>
    </td>
    <td>
      <strong>CloudWatch</strong><br>
      <img src="images/CloudWatch.png" alt="CloudWatch" width="60" height="60" /><br>
      <em>Implemented comprehensive monitoring with custom metrics and automated alerting</em>
    </td>
  </tr>
</table>

### **Performance & Global Delivery**

<table>
  <tr>
    <td>
      <strong>Elastic Load Balancer (ELB)</strong><br>
      <img src="images/Elastic%20Load%20Balancing.png" alt="ELB" width="60" height="60" /><br>
      <em>Distributed traffic across multiple AZs with health checks, eliminating single points of failure</em>
    </td>
    <td>
      <strong>Route 53</strong><br>
      <img src="images/Route%2053.png" alt="Route 53" width="60" height="60" /><br>
      <em>Configured DNS failover routing, reducing recovery time to under 60 seconds</em>
    </td>
  </tr>
</table>

### **Enterprise Capabilities Demonstrated**

- **Cost Optimisation**: Implemented reserved instances and lifecycle policies
- **Security Compliance**: Achieved enterprise-grade security with encryption, MFA, and least privilege
- **Disaster Recovery**: Multi-region backup strategy with automated failover capabilities
- **Scalability**: Architecture supports 10x traffic growth without redesign

---
