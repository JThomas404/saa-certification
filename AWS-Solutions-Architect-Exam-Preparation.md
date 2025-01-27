# AWS Certified Solutions Architect - Associate (SAA-C03) Exam Preparation

This repository documents my journey to achieving the AWS Certified Solutions Architect - Associate (SAA-C03) certification. Each lesson is broken down with detailed steps, problems faced, solutions implemented, and key learning outcomes.

---

## 1. Security and Account Management

### Lesson 1: Learning and Setting Up MFA for the Root User
- **Objective**: Enable Multi-Factor Authentication (MFA) for the root user to ensure secure access to my AWS account.
- **Key Takeaways**: Root users must have MFA enabled, and security is essential from the outset.
- **Screenshots**: ![MFA Setup]()

### Lesson 2: Creating AWS Budgets for Accounts
- **Objective**: Set budgets to monitor AWS costs and avoid overspending.
- **Key Takeaways**: Cost management is a crucial part of AWS account administration.
- **Screenshots**: ![AWS Budget Creation]()

### Lesson 3: Setting Up IAM Accounts for General Access & Production Accounts
- **Objective**: Create IAM roles with custom admin policies for secure access, using MFA instead of the root account.
- **Key Takeaways**: Follow best practices for least privilege and use MFA with IAM users for added security.
- **Screenshots**: ![IAM User Setup]()

### Lesson 4: Setting Up IAM Credentials Using CLI
- **Objective**: Configure IAM credentials using the AWS CLI to automate access management.
- **Key Takeaways**: The AWS CLI simplifies managing permissions and user credentials programmatically.
- **Screenshots**: ![CLI IAM Setup]()

---

## 2. Infrastructure Provisioning and Management

### Lesson 5: Provisioned EC2 Instance and Accessed It with SSH Client
- **Objective**: Provision an EC2 instance and connect to it using SSH.
- **Key Takeaways**: EC2 provides flexible compute resources, and SSH is a secure method of access.
- **Screenshots**: ![EC2 Instance Setup]()

### Lesson 6: Created a Simple S3 Bucket and Uploaded Objects
- **Objective**: Learn how to create an S3 bucket and upload objects.
- **Key Takeaways**: S3 is an essential tool for object storage and managing data in the cloud.
- **Screenshots**: ![S3 Bucket Creation]()

### Lesson 7: Used CloudFormation to Create and Delete EC2 Instances
- **Objective**: Automate the creation and deletion of EC2 instances with CloudFormation.
- **Key Takeaways**: CloudFormation is invaluable for managing infrastructure as code.
- **Screenshots**: ![CloudFormation Setup]()

---

## 3. Automation and Monitoring

### Lesson 8: Created EC2 Instance and Configured a CPU Utilization CloudWatch Alarm
- **Objective**: Set up a CloudWatch alarm to monitor the CPU utilization of an EC2 instance.
- **Key Takeaways**: CloudWatch is vital for monitoring resources, and alarms can help automate resource management.
- **Screenshots**: ![CloudWatch Alarm Setup]()

### Lesson 9: Created an IAM User and Experimented with Assigning Permissions to S3 Buckets
- **Objective**: Experiment with inline policies and managed policies for IAM users to access S3 buckets.
- **Key Takeaways**: IAM policies control access, and understanding them is key to securing resources.
- **Screenshots**: ![IAM Permissions]()

---

## 4. Networking and VPC Design

### Lesson 10: Created an Organization for the Animals4Life Business
- **Objective**: Set up an AWS organization with multiple accounts (General, Production, Development) and configured cross-account roles.
- **Key Takeaways**: Organizations help manage multiple AWS accounts, and cross-account roles simplify permissions management.
- **Screenshots**: ![AWS Organization Setup]()

### Lesson 11: Updated Structure Within the Organization and Applied an SCP
- **Objective**: Applied Service Control Policies (SCPs) to control access and test capabilities within accounts.
- **Key Takeaways**: SCPs enhance governance within AWS Organizations.
- **Screenshots**: ![SCP Configuration]()

### Lesson 12: Created an S3 Bucket for Static Website Hosting
- **Objective**: Create an S3 bucket to host a static website displaying Animals4Life’s top 10 animals.
- **Key Takeaways**: S3’s static website hosting feature simplifies serving web content.
- **Screenshots**: ![S3 Static Website]()

---

## 5. Storage Solutions and Data Management

### Lesson 13: Explored Object Versioning in S3
- **Objective**: Understand how object versioning can prevent data loss and allow recovery of previous file versions.
- **Key Takeaways**: Versioning helps protect data, especially in dynamic applications.
- **Screenshots**: ![S3 Versioning]()

### Lesson 14: Enabled Accelerated Transfer on S3 Bucket
- **Objective**: Set up accelerated transfers in S3 to improve upload speed.
- **Key Takeaways**: S3 acceleration enhances performance when transferring large files.
- **Screenshots**: ![S3 Acceleration]()

### Lesson 15: Created and Configured a KMS Key for Data Encryption
- **Objective**: Set up a KMS key to encrypt and decrypt data stored in S3.
- **Key Takeaways**: KMS is essential for securing data at rest.
- **Screenshots**: ![KMS Key Setup]()

### Lesson 16: Created an S3 Bucket with Multiple Encryption Methods
- **Objective**: Learn about different encryption methods and apply them in S3.
- **Key Takeaways**: Encryption is crucial for ensuring the confidentiality of data.
- **Screenshots**: ![S3 Encryption]()

---

## 6. Database Management

### Lesson 17: Created and Configured Cross-Region Replication (CRR) for S3 Buckets
- **Objective**: Set up CRR to replicate objects across S3 buckets in different regions.
- **Key Takeaways**: CRR ensures that data is available across regions for higher availability.
- **Screenshots**: ![CRR Configuration]()

### Lesson 18: Migrated Database to RDS
- **Objective**: Migrate a WordPress database from EC2 to RDS.
- **Key Takeaways**: RDS simplifies database management and offers high availability features.
- **Screenshots**: ![RDS Migration]()

### Lesson 19: Implemented RDS Multi-AZ Mode and Snapshot Restores
- **Objective**: Set up RDS Multi-AZ for high availability and test snapshot restores.
- **Key Takeaways**: Multi-AZ RDS improves uptime and ensures data durability.
- **Screenshots**: ![RDS Multi-AZ Setup]()

---

## 7. High Availability and Scalability

### Lesson 20: Implemented EFS for Scaling WordPress
- **Objective**: Move WordPress’s static content to EFS for better scalability.
- **Key Takeaways**: EFS provides a scalable file storage solution for multi-instance applications.
- **Screenshots**: ![EFS Setup]()

### Lesson 21: Configured CloudFront Distribution with S3 Origin
- **Objective**: Use CloudFront to deliver content with low latency by caching it at edge locations.
- **Key Takeaways**: CloudFront improves performance and scalability for content delivery.
- **Screenshots**: ![CloudFront Setup]()

---

## 8. Advanced Networking and Security

### Lesson 22: Created an Interface Endpoint for Private EC2 Access
- **Objective**: Configure an interface endpoint to allow private EC2 instance communication within a VPC.
- **Key Takeaways**: Interface endpoints improve security by reducing the need for public IPs.
- **Screenshots**: ![Interface Endpoint]()

### Lesson 23: Implemented Egress-Only Internet Gateway for IPv6 EC2 Instances
- **Objective**: Provide IPv6-enabled instances with internet access while restricting inbound traffic.
- **Key Takeaways**: Egress-only gateways are essential for securing IPv6 instances.
- **Screenshots**: ![Egress-Only Gateway]()

---

## Conclusion

This journey through AWS Solutions Architect exam preparation has been both rewarding and challenging. Each lesson built upon the last, improving my understanding of core AWS services, security practices, and automation techniques. I've not only gained the technical knowledge required for the certification but also developed critical problem-solving skills that will be invaluable in real-world scenarios.

As I continue with my cloud engineering journey, these lessons will serve as a valuable reference. I hope this repository helps others preparing for the exam, offering both a roadmap and insights into what worked for me during the preparation process.
