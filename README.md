# AWS-Cloud-Architecting-Project
A repository for the final capstone project of the AWS Academy Cloud Architecting Course


## Introduction  
### 1. Project Title  
Cloud Architecting Capstone Project: Scalable High‑Availability PHP Web Application for Global Development Statistics  


---

### 2. Project Overview  
The project develops a scalable and highly available PHP web application on AWS for the Example Social Research Organization, a nonprofit, to provide social science researchers with reliable access to global development statistics, such as life expectancy data, addressing the existing website’s issues with growing traffic and security vulnerabilities. It offers secure database hosting via Amazon RDS, anonymous web access through an Application Load Balancer (ALB), and automatic scaling with EC2 instances managed by an Auto Scaling Group (ASG), ensuring researchers can dependably access critical data. Key AWS services include a VPC with public and private subnets, ALB, ASG, RDS for MySQL, and AWS Secrets Manager for secure credential management, delivering a robust and secure solution to support the nonprofit’s mission.

---

## Architecture Diagram  
- Include a detailed architecture diagram of your solution. You can use tools like **Lucidchart**, **Draw.io**, or **AWS Architecture Diagramming Tool**.  

**Checklist:**  
- [ ] Does the diagram include all key components (e.g., VPC, subnets, load balancers, EC2 instances, S3 buckets)?  
- [ ] Are security services like IAM roles, security groups, and KMS indicated?  
- [ ] Is the flow of data/workload clearly illustrated?  

---

## Features and Functionality  
### 1. Key Features    
  
- `Autoscaling`: EC2 Auto Scaling group with target tracking policies for CPU utilization.  
- `High Availability`: Multi‑AZ Amazon RDS and EC2 instances behind an Application Load Balancer.
- `Secure Secrets Management`: Credentials stored and rotated in AWS Secrets Manager.
- `Network Segmentation`: Application and database servers in private subnets; only ALB and Bastion host are public.
- `SSH Access`: Bastion host with restricted IP access for administrators.
  

### 2. AWS Services Used    
  
- `Amazon EC2`: Hosts the web servers that run the application, providing the compute capacity needed to process requests and deliver content to users.  
- `Amazon RDS`: Hosts the relational database that stores the application’s data, offering a managed database solution with automated backups and scalability.
- `AWS Auto Scaling`: Manages the scaling of EC2 instances to match demand, ensuring the application adapts dynamically to traffic fluctuations.
- `Application Load Balancer`: Distributes HTTP requests across EC2 instances.
- `AWS Secrets Manager`: Secure storage and automatic rotation of DB credentials.
- `IAM`: Roles granting least-privilege access.
- `Amazon VPC`: Network isolation with public and private subnets.
- `Security Groups & NACLs`: Network-level access controls.

---

## Deployment  
### 1. Prerequisites  
- List any software, tools, or AWS configurations required to deploy the project.  

**Example:**  
- `AWS CLI` installed and configured.  
- IAM user with admin privileges.  

### 2. Step-by-Step Deployment Instructions  
- Provide a clear, concise set of steps for deploying the project.  

**Checklist:**  
- [ ] Include instructions for launching CloudFormation templates or Terraform scripts (if applicable).  
- [ ] Detail any manual configurations in the AWS Management Console.  

---

## Security  
- Describe security measures implemented in your architecture.  

**Example:**  
- `IAM Roles`: Restrict access to resources based on least privilege.  
- `Encryption`: S3 bucket encryption using SSE-KMS.  
- `Network Security`: Configured security groups and NACLs.  

---

## Testing and Validation  
### 1. Testing Strategy  
- Describe how the project was tested, including tools used (e.g., Postman, AWS CloudWatch Logs).  

**Checklist:**  
- [ ] What tests were conducted (e.g., load testing, failover testing)?  
- [ ] Include commands, test cases, or examples.  

---

## Challenges and Learnings  
- Reflect on any challenges faced during implementation and what you learned from them.  

**Example:**  
- Challenge: Setting up an ALB to route traffic between subnets.  
- Learning: Gained hands-on experience with cross-zone load balancing.  

---

## Future Improvements  
- Suggest potential upgrades or optimizations for the project.  

**Example:**  
- Implement CI/CD using AWS CodePipeline.  
- Enhance monitoring with Amazon CloudWatch Insights.

---

## Contributors  
 
`Peter Brian Mwangi - Implementation and project documentation`

---

## License  
- Include licensing information for your project (if applicable).  

**Example:**  
This project is licensed under the MIT License.

---
