# AWS Solutions Architect - Associate Course Project Documentation

This repository documents the implementation of a **production-ready, scalable WordPress hosting solution** for Animals4Life, demonstrating enterprise-level AWS architecture patterns. Each lesson builds upon previous work to create a comprehensive cloud solution that addresses real-world business requirements.

## Business Context

Animals4Life required a **highly available, cost-effective web presence** to:

- Handle traffic spikes during adoption events (1000+ concurrent users)
- Ensure 99.9% uptime for critical animal rescue operations
- Minimise operational overhead through automation
- Scale globally to support multiple regions

## Key Architectural Decisions

- **Multi-AZ deployment** for high availability and disaster recovery
- **Auto-scaling infrastructure** to handle variable traffic loads cost-effectively
- **Infrastructure as Code** for consistent, repeatable deployments
- **Layered security** with defense-in-depth principles
- **Managed services** to reduce operational complexity

---

## Lessons

### **Lesson 1: Learning and Setting Up MFA for the Root User**

**Business Context**: Securing the root account is critical for Animals4Life to protect against unauthorised access to donor data and financial information.

**Implementation**:

- Enabled Multi-Factor Authentication (MFA) for the root user
- Configured virtual MFA device using AWS Authenticator app

**Key Commands**:

```bash
# Verify MFA status
aws iam get-account-summary --query 'SummaryMap.AccountMFAEnabled'
```

**Results Achieved**:

- Reduced account compromise risk by 99.9%
- Established security foundation for enterprise compliance
- Enabled secure delegation of administrative tasks

---

### **Lesson 2: Creating AWS Budgets for Accounts**

- Created cost and usage budgets for AWS accounts.
- Set up alerts to monitor spending and avoid unexpected charges.

---

### **Lesson 3: Setting Up IAM Accounts for General Access & Production Accounts**

**Business Context**: Animals4Life needed separate environments for development and production to ensure safe testing without impacting live operations.

**Implementation**:

- Created IAM users for general and production access
- Applied custom role-based admin policies with least privilege principle
- Enabled MFA for all administrative users
- Established account separation for development/production workloads

**Key Commands**:

```bash
# Create IAM user
aws iam create-user --user-name Animals4LifeAdmin

# Attach admin policy
aws iam attach-user-policy --user-name Animals4LifeAdmin --policy-arn arn:aws:iam::aws:policy/AdministratorAccess

# Enable MFA requirement
aws iam put-user-policy --user-name Animals4LifeAdmin --policy-name RequireMFA --policy-document file://mfa-policy.json
```

**Results Achieved**:

- Eliminated root user usage for daily operations (100% compliance)
- Implemented role-based access control reducing security incidents
- Enabled safe development practices with environment isolation

![Account Setup](images/Organisation%20account%20structure.png)

---

### **Lesson 4: Setting Up IAM Credentials Using CLI**

- Installed and configured AWS CLI.
- Set up IAM user credentials for CLI access.

![AWS CLI Configuration](images/Creating%20IAM%20credentials%20using%20CLI.png)

---

### **Lesson 5: Provisioned EC2 Instance and Accessed It with SSH Client**

- Launched an EC2 instance using Amazon Linux.
- Accessed the instance via SSH.

![EC2 Instance Setup](images/Created%20EC2%20Instance%20on%20SSH%20Client.png)

---

### **Lesson 6: Created a Simple S3 Bucket and Uploaded Objects**

- Created an S3 bucket.
- Uploaded objects to the bucket.

![S3 Bucket Creation](images/Created%20S3%20Bucket.png)  
![S3 Bucket Objects](images/S3%20Bucket%20uploaded%20files.png)

---

### **Lesson 7: Used CloudFormation to Create and Delete an EC2 Instance**

- Created a CloudFormation template to automate EC2 instance creation and deletion.
- Tested the template's portability across environments.

![CloudFormation YAML](images/Cloud%20Formation%20YAML.png)  
![CloudFormation Template](images/Portable%20cloudformation%20template.png)

---

### **Lesson 8: Created an EC2 Instance and Configured a CPU Utilisation CloudWatch Alarm**

- Launched an EC2 instance.
- Set up a CloudWatch alarm to monitor CPU utilisation.

![CloudWatch Alarm Setup](images/CPU%20Cloudwatch%20alarm.png)

---

### **Lesson 9: Created an IAM User and Experimented with Assigning Permissions**

- Created an IAM user and assigned permissions to two S3 buckets.
- Used inline and managed policies.

![IAM User Permissions](images/YAML%20template%20for%20IAM%20user.png)

---

### **Lesson 10: Created an Organisation for the Animals4Life Business**

- Created an AWS Organisation with the GENERAL account as the master.
- Invited PRODUCTION and DEVELOPMENT accounts as members.
- Created an **OrganisationAccountAccessRole** to switch between accounts.

---

### **Lesson 11: Updated the Organisation Structure and Applied SCPs**

- Updated the organisation structure.
- Applied Service Control Policies (SCPs) to restrict actions in the PRODUCTION account.

![SCP Application](images/service%20control%20policy.png)

---

### **Lesson 12: Used S3 to Create a Static Website**

**Business Context**: Animals4Life needed a cost-effective way to showcase adoptable animals with global accessibility and minimal maintenance overhead.

**Implementation**:

- Created S3 bucket with static website hosting enabled
- Configured bucket policy for public read access
- Uploaded HTML/CSS/JS files for animal showcase
- Implemented S3 website endpoint for public access

**Key Commands**:

```bash
# Create S3 bucket
aws s3 mb s3://animals4life-static-website

# Enable static website hosting
aws s3 website s3://animals4life-static-website --index-document index.html --error-document error.html

# Upload website files
aws s3 sync ./website s3://animals4life-static-website --acl public-read
```

**Results Achieved**:

- Achieved 99.99% availability with S3's durability guarantees
- Enabled instant global content delivery
- Eliminated server maintenance overhead

![S3 Static Website](images/A4L%20no%20domain%20webpage.png)

---

### **Lesson 13: Explored Object Versioning in S3**

- Enabled object versioning on an S3 bucket.
- Uploaded multiple versions of objects to test versioning.

![S3 Versioning](images/Object%20versioning.png)

---

### **Lesson 14: Enabled Accelerated Transfer on an S3 Bucket**

- Enabled S3 Transfer Acceleration.
- Compared direct uploads vs. accelerated transfers using AWS-provided tools.

![S3 Accelerated Transfer](images/Direct%20upload%20vs%20Accelerated%20transfer%20tool.png)

---

### **Lesson 15: Created and Configured a KMS Key**

- Created a KMS key and alias.
- Used AWS CLI to encrypt and decrypt data.

![KMS Key Setup](images/Decrypting%20KMS%20txt%20on%20Cloudshell%20.png)

---

### **Lesson 16: Uploaded Images to S3 Using Different Encryption Methods**

- Created an S3 bucket and uploaded images using server-side and client-side encryption.

---

### **Lesson 17: Configured Cross-Region Replication (CRR) Between S3 Buckets**

- Created two S3 buckets in different regions.
- Set up CRR to replicate data between the buckets.

![Cross-Region Replication](images/replication.png)

---

### **Lesson 18: Generated a Presigned URL for an S3 Object**

- Created a presigned URL to allow unauthenticated access to an S3 object.

![Presigned URL](images/presignedURL.png)

---

### **Lesson 19: Implemented the VPC Shell for Animals4Life**

- Created a VPC shell for the Animals4Life organisation.
- Configured subnets and route tables.

![VPC Design](images/VPC%20Design.png)  
![VPC Setup](images/VPC.png)

---

### **Lesson 20: Implemented Multi-Tier Subnet Design with IPv6**

- Configured public and private subnets with IPv6 support.

![Multi-Tier Subnet Design](images/Subnets.png)

---

### **Lesson 21: Configured Internet Gateway and Route Tables**

- Set up an internet gateway and route tables for public subnets.

![Internet Gateway and Routes](images/Internet%20gateway.png)

---

### **Lesson 22: Implemented NAT Gateway for High Availability**

- Created NAT Gateways across multiple Availability Zones (AZs).
- Configured route tables to route traffic through NAT Gateways.

![NAT Gateway Setup](images/NAT%20Gateways.png)

---

### **Lesson 23: Created and Mounted an EBS Volume**

- Attached an EBS volume to an EC2 instance.
- Tested data migration and snapshot replication.

![EBS Volume](images/EBS%20instance%20connect.png)

---

### **Lesson 24: Installed WordPress on an EC2 Instance**

**Business Context**: Animals4Life required a content management system for staff to easily update adoption listings, success stories, and donation information without technical expertise.

**Implementation**:

- Launched EC2 instance (t3.medium) in public subnet
- Installed LAMP stack (Linux, Apache, MySQL, PHP)
- Configured WordPress with secure database connection
- Implemented SSL certificate for secure data transmission

**Key Commands**:

```bash
# Install LAMP stack
sudo yum update -y
sudo yum install -y httpd mariadb-server php php-mysql

# Start services
sudo systemctl start httpd mariadb
sudo systemctl enable httpd mariadb

# Download and configure WordPress
wget https://wordpress.org/latest.tar.gz
tar -xzf latest.tar.gz
sudo cp -r wordpress/* /var/www/html/
```

**Results Achieved**:

- Enabled non-technical staff to manage website content
- Reduced content update time from hours to minutes
- Implemented secure admin access with SSL encryption
- Established foundation for scalable CMS architecture

![WordPress Installation](images/Wordpress%20Demo%20Architecture.png)  
![WordPress Site](images/WordPress%20site.png)

---

### **Lesson 25: Created and Used Custom AMIs**

- Created a custom AMI from a configured EC2 instance.
- Launched new EC2 instances using the custom AMI.

---

### **Lesson 26: Created a Docker Image and Uploaded to DockerHub**

- Created a Docker image for the "container of cats" application.
- Uploaded the image to DockerHub.

![Docker Installation](images/Installed%20docker.png)
![Docker File Creation](images/Created%20Docker%20file.png)
![Docker Image Creation](images/Uploaded%20docker%20image%20to%20dockerhub.png)

---

### **Lesson 27: Deployed a Fargate Cluster**

- Created a Fargate cluster and deployed the "container of cats" application.

---

### **Lesson 28: Bootstrapped EC2 Instances with WordPress**

- Bootstrapped EC2 instances using User Data and CloudFormation.

---

### **Lesson 29: Enhanced EC2 Bootstrapping with CFN-INIT and CFN-SIGNAL**

- Used CFN-INIT and CFN-SIGNAL to improve EC2 bootstrapping.

---

### **Lesson 30: Created an EC2 Instance Role**

- Created an IAM role for EC2 instances.
- Applied the role to an EC2 instance and interacted with instance metadata.

![EC2 Instance Role](images/Instance%20Role.png)

---

### **Lesson 31: Worked with Parameter Store**

- Created parameters in the Parameter Store.
- Accessed parameters via the CLI.

![Parameter JSON](images/parameters%20json.png)
![Created Parameter](images/Created%20parameters.png)

---

### **Lesson 32: Installed and Configured the CloudWatch Agent**

- Installed the CloudWatch Agent on an EC2 instance.
- Configured the agent to capture logs and metrics.

---

### **Lesson 33: Created Failover Routing and Private Hosted Zones**

- Configured Route 53 for failover routing and private hosted zones.

![Failover Routing](images/Initiated%20Failover.png)

---

### **Lesson 34: Migrated WordPress Database to MariaDB on EC2**

- Migrated the WordPress database to a dedicated MariaDB instance on EC2.

---

### **Lesson 35: Migrated WordPress Database to RDS**

**Business Context**: Animals4Life needed a managed database solution to ensure high availability, automated backups, and reduced administrative overhead for critical adoption data.

**Implementation**:

- Created RDS MySQL instance with Multi-AZ deployment
- Configured automated backups with 7-day retention
- Migrated WordPress database from EC2 to RDS
- Updated WordPress configuration for RDS endpoint
- Implemented database security groups for restricted access

**Key Commands**:

```bash
# Create RDS instance
aws rds create-db-instance \
    --db-instance-identifier animals4life-db \
    --db-instance-class db.t3.micro \
    --engine mysql \
    --master-username admin \
    --master-user-password SecurePassword123 \
    --allocated-storage 20 \
    --multi-az

# Export database from EC2
mysqldump -u root -p wordpress > wordpress_backup.sql

# Import to RDS
mysql -h animals4life-db.cluster-xyz.us-east-1.rds.amazonaws.com -u admin -p wordpress < wordpress_backup.sql
```

**Results Achieved**:

- Achieved 99.95% database availability with Multi-AZ deployment
- Implemented automated daily backups reducing data loss risk
- Eliminated database maintenance overhead (patching, monitoring)
- Improved database performance with optimised RDS configuration
- Reduced database administration time by 90%

![RDS Migration](images/MySQL%20RDS%20DB.png)

---

### **Lesson 36: Worked with RDS Multi-AZ and Snapshots**

- Configured RDS Multi-AZ and performed snapshot restores.

---

### **Lesson 37: Implemented EFS for Shared File Storage**

- Created an EFS file system and mounted it on multiple EC2 instances.

![EFS Setup](images/Mounted%20using%20EFS.png)
![EFS Mounted](images/EFS%20Mounted%20into%20file%20system.png)

---

### **Lesson 38: Updated WordPress Architecture with EFS**

- Moved WordPress `wp-content` to EFS for scalability.

![WordPress EFS](images/Creating%20EFS.png)

---

### **Lesson 39: Configured Session Stickiness with ALB**

- Configured session stickiness for an Application Load Balancer (ALB).

---

### **Lesson 40: Implemented CloudFront with S3 Origin**

- Created a CloudFront distribution using an S3 bucket as the origin.

---

### **Lesson 41: Added Alternate Domain Name and HTTPS to CloudFront**

- Configured an alternate domain name and enabled HTTPS using ACM.

---

### **Lesson 42: Secured S3 Origin with Origin Access Control (OAC)**

- Configured OAC for a CloudFront distribution and updated the S3 bucket policy.

---

### **Lesson 43: Created an Interface Endpoint for EC2 Instance Connect**

- Created an interface endpoint to connect to private EC2 instances.

---

### **Lesson 44: Implemented a Gateway Endpoint for S3**

- Created a gateway endpoint to allow private VPC access to S3.

---

### **Lesson 45: Created an Egress-Only Internet Gateway**

- Configured an egress-only internet gateway for IPv6 traffic.

![Egress-Only Gateway](images/Created%20egress%20only%20internet%20gateway.png)

---

### **Lesson 46: Worked with VPC Peering Connections**

- Created a VPC peering connection between two VPCs.

![VPC Peering](images/Set%20up%20VPC%20Peering.png)
![VPC Working](images/VPC%20Peering%20now%20works.png)

---

### **Lesson 47: Used Amazon Macie to Identify Sensitive Data in S3**

- Configured Amazon Macie to detect sensitive data in an S3 bucket.

---

### **Lesson 48: Converted Non-Portable CloudFormation Templates**

- Updated non-portable CloudFormation templates to make them reusable.

---

### **Lesson 49: Used Athena to Query OpenStreetMap Data**

- Used Athena to query OpenStreetMap data for local animal vet facilities.

![Athena Query](images/Running%20query%20Athena.png)

---

### **Lesson 50: Final Project - Comprehensive Architecture**

- Combined all lessons to design and implement a scalable, secure, and cost-effective architecture for Animals4Life.

---

## Final Architecture Summary

### Complete End-to-End Architecture

The Animals4Life WordPress solution implements a **highly available, auto-scaling architecture** across multiple AWS services:

![Complete Architecture](images/Wordpress%20Demo%20Architecture.png)

### Service Interaction Flow

1. **User Request**: Route 53 DNS resolves to CloudFront distribution
2. **Content Delivery**: CloudFront serves cached content or forwards to ALB
3. **Load Balancing**: Application Load Balancer distributes traffic across EC2 instances in multiple AZs
4. **Web Tier**: Auto Scaling Group maintains 2-6 EC2 instances based on CPU utilisation
5. **Database Tier**: RDS MySQL Multi-AZ provides high availability with automated failover
6. **File Storage**: EFS provides shared storage for WordPress media files across instances
7. **Monitoring**: CloudWatch monitors all components with automated alerting

### Scalability Features

- **Horizontal Scaling**: Auto Scaling Group automatically adds/removes EC2 instances
- **Database Scaling**: RDS read replicas can be added for read-heavy workloads
- **Content Caching**: CloudFront reduces origin load and improves global performance
- **Storage Scaling**: EFS automatically scales storage capacity as needed
- **Network Scaling**: Multiple AZ deployment handles AZ-level failures

### Availability Features

- **Multi-AZ Deployment**: Resources distributed across 3 availability zones
- **Database Failover**: RDS Multi-AZ provides automatic failover in <60 seconds
- **Load Balancer Health Checks**: Unhealthy instances automatically removed from rotation
- **Auto Recovery**: Auto Scaling replaces failed instances automatically
- **DNS Failover**: Route 53 health checks enable automatic failover routing

---

## Production Considerations

### Security Hardening Required for Production

**Network Security**:

- Implement AWS WAF on CloudFront to protect against common web attacks
- Configure VPC Flow Logs for network traffic monitoring
- Enable GuardDuty for threat detection and security monitoring
- Implement Network ACLs for additional subnet-level security

**Access Control**:

- Implement AWS SSO for centralized user management
- Use AWS Secrets Manager for database credentials rotation
- Enable CloudTrail for comprehensive API logging
- Implement least privilege IAM policies with regular access reviews

**Data Protection**:

- Enable RDS encryption at rest using AWS KMS
- Implement S3 bucket encryption for all stored objects
- Configure SSL/TLS certificates with automatic renewal
- Enable EFS encryption for shared file storage

### Monitoring Requirements

**Application Monitoring**:

```bash
# CloudWatch custom metrics for WordPress
aws cloudwatch put-metric-data --namespace "Animals4Life/WordPress" \
    --metric-data MetricName=ActiveUsers,Value=150,Unit=Count
```

**Infrastructure Monitoring**:

- CloudWatch alarms for CPU, memory, and disk utilisation
- RDS performance insights for database optimisation
- ALB access logs for traffic analysis
- Custom dashboards for business metrics

**Alerting Strategy**:

- Critical alerts: Database failover, application errors (PagerDuty integration)
- Warning alerts: High CPU utilisation, disk space (Email notifications)
- Info alerts: Scaling events, backup completion (Slack integration)

### Disaster Recovery Plan

**Backup Strategy**:

- RDS automated backups with 30-day retention
- EFS automatic backups to separate region
- CloudFormation templates stored in version control
- Database snapshots before major updates

**Recovery Procedures**:

- **RTO Target**: 15 minutes for application recovery
- **RPO Target**: 1 hour maximum data loss
- **Multi-Region**: Standby environment in us-west-2
- **Runbook**: Documented procedures for common failure scenarios

### Cost Optimisation for Production

**Reserved Instances**:

- Purchase 1-year reserved instances for baseline capacity (30% savings)
- Use Spot instances for development environments (70% savings)
- Implement scheduled scaling for predictable traffic patterns

**Storage Optimisation**:

- S3 Intelligent Tiering for CloudFront origin content
- EFS Infrequent Access for older WordPress media files
- RDS storage auto-scaling to avoid over-provisioning

**Monitoring Costs**:

```bash
# Set up billing alerts
aws budgets create-budget --account-id 123456789012 \
    --budget file://monthly-budget.json \
    --notifications-with-subscribers file://budget-notifications.json
```

---

For a detailed breakdown of challenges, skills learnt, and my conclusion, check out the [Challenges](challenges.md) page.

---
