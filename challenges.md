Here’s the revised version of your document with improved formatting, grammar, and consistency. I’ve also fixed minor issues and ensured the content flows smoothly:

---

# Challenges, Skills Learned, and Conclusion

Throughout my AWS Solutions Architect – Associate (SAA-C03) course project, I encountered several challenges that tested my problem-solving skills and deepened my understanding of AWS services. Below, I discuss these challenges, how I overcame them, the skills I acquired, and a conclusion summarizing my journey.

---

## Challenges and How I Overcame Them

### 1. S3 Bucket Access Issues  
While creating a static website on S3, I encountered a `403 Access Denied` error despite configuring the bucket policy correctly. Upon further investigation, I discovered the issue was due to the **Object Ownership** setting. By changing it to **Bucket Owner Preferred** and re-uploading the objects, I resolved the issue. This experience taught me the importance of always checking **Object Ownership** settings when troubleshooting S3 access issues.

---

### 2. CloudFormation Template Errors  
When creating a CloudFormation template to automate EC2 instance creation, I encountered syntax errors that caused the stack to fail. I used the AWS CloudFormation Designer to validate the template and corrected the errors. This challenge reinforced the need to always validate CloudFormation templates before deployment and use tools like CloudFormation Designer for debugging.

---

### 3. CloudFront Distribution Misconfiguration  
My CloudFront distribution failed to deliver content from the S3 origin due to incorrect cache settings. I adjusted the cache settings and ensured the S3 bucket policy allowed CloudFront access. This experience highlighted the importance of double-checking cache settings and origin access policies when configuring CloudFront.

---

## Skills I Have Learned

### 1. Hands-On Experience with Core AWS Services  
- Gained practical experience with **EC2**, **S3**, **RDS**, **CloudFormation**, **CloudFront**, **IAM**, and **VPC**.  
- Learned how to configure, secure, and optimize these services for real-world use cases.  

---

### 2. Troubleshooting and Debugging  
- Developed strong troubleshooting skills by resolving issues like S3 access errors, CloudFormation failures, and RDS connectivity problems.  
- Applied these skills in real-world scenarios, such as in my [SQL Maintenance Plan Project](https://github.com/JThomas404/SQL-Maintenance-Plan-Project/blob/main/README.md).  
- Learned to use AWS tools such as **CloudWatch Logs** and **CloudTrail** for debugging.  

---

### 3. Infrastructure as Code (IaC)  
- Built my projects using **Terraform** to automate infrastructure deployment.  
- Learned how to create reusable and portable templates.  

---

### 4. Security Best Practices  
- Implemented **MFA**, **IAM roles**, **SCPs**, and **encryption** to secure AWS resources.  
- Learned how to configure **KMS** for encryption and **CloudFront** for secure content delivery.  

---

### 5. Scalability and High Availability  
- Designed scalable architectures using **Auto Scaling**, **ELB**, and **EFS**.  
- Configured **Multi-AZ RDS** and **NAT Gateways** to ensure high availability.  

---

### 6. Cost Management  
- Created **AWS Budgets** and used **Cost Explorer** to monitor and optimize costs.  
- Learned how to use **S3 Lifecycle Policies** to reduce storage costs.  

---

### 7. Serverless and Containerization  
- Gained experience with **AWS Lambda**, **API Gateway**, and **Fargate** for serverless and containerized applications.  
- Learned how to deploy and manage Docker containers using **ECR** and **Fargate**.  

---

### 8. Networking and Connectivity  
- Configured **VPCs**, **subnets**, **route tables**, **NAT Gateways**, and **VPC peering**.  
- Learned how to set up **CloudFront** and **Route 53** for global content delivery and DNS management.  

---

## Conclusion

This AWS Solutions Architect – Associate course project has been an incredible learning experience. I gained hands-on experience with a wide range of AWS services, from foundational tools like EC2 and S3 to advanced features like CloudFormation, RDS, and CloudFront. Along the way, I encountered and overcame numerous challenges, which taught me the importance of thorough testing, debugging, and adherence to best practices.

The skills I have acquired—ranging from infrastructure automation and security to scalability and cost optimization—have prepared me to design and implement robust, secure, and cost-effective cloud architectures. This project has not only helped me prepare for the AWS SAA-C03 certification but also equipped me with practical knowledge that I can apply in real-world scenarios.

As I move forward, I am excited to continue exploring AWS services, deepen my expertise, and contribute to building innovative cloud solutions. This journey has been challenging but immensely rewarding, and I am confident that the skills I have developed will serve as a strong foundation for my career in cloud architecture.