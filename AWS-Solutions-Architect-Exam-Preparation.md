# AWS Certified Solutions Architect - Associate (SAA-C03) Exam Preparation

This repository documents my journey to achieving the AWS Certified Solutions Architect - Associate (SAA-C03) certification. Each lesson is broken down with detailed steps, problems faced, solutions implemented, and key learning outcomes. The aim is to provide a transparent and thorough look at my journey, showcasing my growing skills in cloud architecture.

---

## Lesson 1: Enabling MFA for the Root User

**Objective:**  
Secure the AWS account by enabling Multi-Factor Authentication (MFA) for the root user.

**Actions Taken:**  
- Logged into AWS Management Console as the root user and accessed the MFA settings.
- Chose an authenticator app (Google Authenticator) and followed the setup instructions to link it with the root user account.

**Key Takeaways:**  
- Implementing MFA is an essential step for securing sensitive AWS accounts, particularly the root user, which has unrestricted access to the entire account.
- This reinforced my understanding of AWS security best practices and the importance of mitigating risks.

**Challenges:**  
- There were no major obstacles during this process. However, I had to ensure the authenticator app was properly synchronized to avoid access issues later.

**What I Would Do Differently:**  
- I would recommend always keeping a backup method (like SMS or another app) to prevent any lockout issues in case the primary authenticator fails.

---

## Lesson 2: Setting Up AWS Budgets for Account Cost Monitoring

**Objective:**  
Create AWS Budgets to track and alert on cost thresholds across AWS accounts.

**Actions Taken:**  
- Went into the AWS Budgets dashboard and created a budget to monitor costs for EC2 usage and S3 storage.
- Set up alert thresholds to notify me when spending reached 70% and 90% of my budget limit.
- Configured email notifications for these alerts to ensure timely awareness of potential overspending.

**Key Takeaways:**  
- AWS Budgets is a powerful tool for keeping cloud spending within expected limits. The ability to set up alerts helps avoid costly surprises.
- This exercise helped me become familiar with cost optimization strategies in AWS, something crucial for any solutions architect.

**Challenges:**  
- Configuring the alerts across multiple accounts within the same organization took a bit of time and was slightly confusing at first.
- I had to read through AWS documentation to figure out how to manage cross-account alerts correctly, which was a bit challenging.

**What I Learned:**  
- Understanding and managing costs effectively in AWS is essential for maintaining a sustainable cloud architecture.
- AWS Budgets can be part of a broader cost management strategy, working alongside tools like AWS Cost Explorer and Trusted Advisor.

---

## Lesson 3: Creating IAM Users and Configuring Permissions

**Objective:**  
Create IAM users for both general and production access with appropriate permissions.

**Actions Taken:**  
- Created separate IAM users for each team member and assigned them distinct permissions based on their roles (General, Admin, Production).
- Configured MFA for each user to enhance account security.
- Explored IAM policies, particularly managing permissions using AWS-managed policies and custom inline policies.

**Key Takeaways:**  
- The Principle of Least Privilege (PoLP) is fundamental in creating secure IAM users.
- Each IAM user should only have the permissions necessary for their role, which minimizes security risks.

**Challenges:**  
- One major challenge was figuring out the right policies for the production environment. I was unsure about how restrictive to make the permissions, which led to a couple of trial and error configurations.
- After researching best practices, I refined my understanding of how IAM roles and policies work.

**What I Would Do Differently:**  
- I would have spent more time exploring the IAM Access Analyzer to ensure that there were no unintended security gaps.
- Creating clear documentation on roles and policies would make future audits and user modifications easier.

---

## Lesson 4: Launching and Managing EC2 Instances

**Objective:**  
Launch EC2 instances and configure secure access using security groups and key pairs.

**Actions Taken:**  
- Launched an EC2 instance using the Amazon Linux 2 AMI and selected the t2.micro instance type for cost efficiency.
- Created a security group that allowed SSH access only from a specific IP range to minimize exposure.
- Generated a key pair for SSH access and used it to connect to the EC2 instance.

**Key Takeaways:**  
- EC2 instances are the backbone of many AWS workloads. It's essential to configure them properly from the start to ensure both performance and security.
- Security groups and key pairs are critical for controlling access to EC2 instances, especially when deployed in a production environment.

**Challenges:**  
- The main issue I faced was misconfiguring security group settings, which initially blocked my SSH access. I had to troubleshoot the inbound rules to ensure that the correct IP was whitelisted.
- Understanding how security groups interact with EC2 instances took some time, but I learned how to fine-tune the settings based on specific use cases.

**What I Learned:**  
- Best practices for EC2 include using only the necessary ports, applying strict security groups, and always ensuring that key pairs are securely managed.
- I now better understand the risks of leaving default security group settings in place and the importance of tightening security in cloud environments.

---

## Lesson 5: Managing S3 Buckets and Versioning

**Objective:**  
Set up S3 buckets for object storage and enable versioning for file management.

**Actions Taken:**  
- Created an S3 bucket to store sample files, configured versioning to allow rollback to previous versions, and set lifecycle rules to manage object expiration.
- Tested versioning by uploading new versions of a file and retrieving them later.

**Key Takeaways:**  
- S3 is a powerful object storage service that can be optimized using versioning and lifecycle policies.
- Versioning in S3 helps prevent data loss and provides an effective way to recover previous file states.

**Challenges:**  
- I initially had some confusion regarding the differences between bucket policies and IAM policies. It took a few attempts to clarify when to use each one and how they interact.

**What I Would Do Differently:**  
- I would configure more granular lifecycle policies and enable cross-region replication for increased data durability and availability.
- In future implementations, I would ensure access controls are tightly managed using both bucket and IAM policies.

---

## Conclusion

This journey through AWS Solutions Architect exam preparation has been both rewarding and challenging. Each lesson built upon the last, improving my understanding of core AWS services, security practices, and automation techniques. I've not only gained the technical knowledge required for the certification but also developed critical problem-solving skills that will be invaluable in real-world scenarios. 
