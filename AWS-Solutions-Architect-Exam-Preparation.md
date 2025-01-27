# AWS Certified Solutions Architect - Associate (SAA-C03) Exam Preparation

This repository documents my journey to achieving the AWS Certified Solutions Architect - Associate (SAA-C03) certification. It provides a comprehensive breakdown of each lesson I undertook during my preparation process, detailing the tasks performed, insights gained, and challenges faced. This approach will showcase my practical experience with AWS and demonstrate my problem-solving skills.

## Lesson Overview

### Lesson 1: Enabling MFA for the Root User

**Objective:**  
Secure AWS account by enabling Multi-Factor Authentication (MFA) for the root user.

**Actions Taken:**  
- Logged into AWS Management Console as root user.
- Enabled MFA using an authenticator app.

**Key Takeaways:**  
- MFA is a vital security measure to protect high-privilege AWS accounts.
- This step reinforced the importance of securing the root user account.

**Challenges:**  
- The process was straightforward with no significant challenges.

### Lesson 2: Setting Up AWS Budgets for Account Cost Monitoring

**Objective:**  
Create AWS Budgets to track and alert on cost thresholds across AWS accounts.

**Actions Taken:**  
- Created and configured AWS Budgets for monitoring service costs.
- Set up alert notifications for budget thresholds.

**Key Takeaways:**  
- AWS Budgets is a vital tool for managing costs effectively in a cloud environment.
- Configuring alerts helps prevent unexpected charges.

**Challenges:**  
- Configuring cross-account alerts for budgets was initially confusing, but thorough reading of AWS documentation resolved the issue.

**Screenshots:**  
- [Include screenshots of budget creation and alert configuration process]

### Lesson 3: Creating IAM Users and Configuring Permissions

**Objective:**  
Create IAM users for general and production access with appropriate permissions.

**Actions Taken:**  
- Created IAM users for both general and production environments.
- Configured MFA for each user and assigned appropriate roles.

**Key Takeaways:**  
- Principle of least privilege is essential when assigning permissions.
- Ensuring each IAM user has the correct permissions minimizes security risks.

**Challenges:**  
- Encountered difficulty in fine-tuning permissions for the production environment. Resolved by better understanding IAM roles and policies.

**Screenshots:**  
- [Include screenshots of IAM user setup and role configuration]

### Lesson 4: Launching and Managing EC2 Instances

**Objective:**  
Launch EC2 instances and configure secure access using security groups and key pairs.

**Actions Taken:**  
- Launched an EC2 instance with Amazon Linux 2 AMI.
- Configured a security group to allow SSH access only from a specified IP.
- Accessed the EC2 instance via SSH using a key pair.

**Key Takeaways:**  
- EC2 instances are fundamental compute resources in AWS.
- Proper configuration of security groups and key pairs is critical to securing access.

**Challenges:**  
- Configuring the correct security group settings and ensuring SSH access from only my IP address was initially challenging.

**Screenshots:**  
- [Include screenshots of EC2 setup and security group configuration]

### Lesson 5: Managing S3 Buckets and Versioning

**Objective:**  
Set up S3 buckets for object storage and enable versioning for file management.

**Actions Taken:**  
- Created an S3 bucket for file storage.
- Enabled versioning to track and recover object versions.

**Key Takeaways:**  
- S3 offers scalable and durable object storage.
- Versioning is useful for managing file changes and enabling recovery.

**Challenges:**  
- Initial confusion with the differences between bucket policies and IAM policies. Gained clarity through AWS documentation.

**Screenshots:**  
- [Include screenshots of S3 bucket creation and versioning setup]

### Lesson 6: Automating EC2 Provisioning with CloudFormation

**Objective:**  
Use CloudFormation to automate the creation of EC2 instances.

**Actions Taken:**  
- Created a CloudFormation template to provision EC2 instances.
- Launched a stack using the template.

**Key Takeaways:**  
- CloudFormation allows for Infrastructure as Code (IaC), automating the provisioning of AWS resources.
- Familiarity with YAML syntax and CloudFormation resources is critical for repeatable infrastructure setups.

**Challenges:**  
- Learning the YAML syntax for CloudFormation templates and troubleshooting errors in the configuration was challenging.

**Screenshots:**  
- [Include screenshots of CloudFormation template and EC2 instance deployment]

...

## Conclusion

The AWS Solutions Architect certification process has been both challenging and rewarding. Through each lesson, I gained a deeper understanding of key AWS services, security best practices, and automation techniques. The hands-on experience of configuring and managing AWS resources has significantly improved my cloud architecture skills, positioning me well for real-world AWS implementations.

This journey not only helped me prepare for the certification exam but also gave me the confidence to work on large-scale cloud projects. I'm excited to continue building on this knowledge and applying it to professional cloud engineering tasks.
