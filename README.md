#**🛡️ DevSecOps CI/CD Pipeline with Terraform, Jenkins & Trivy**
Secure Infrastructure Deployment with Automated Security Scanning

This project demonstrates a DevSecOps pipeline that automates infrastructure provisioning, container image creation, vulnerability scanning, and deployment on AWS.

The pipeline integrates Terraform for Infrastructure as Code, Docker for containerization, and Trivy for security scanning within a Jenkins CI/CD pipeline. The goal is to detect security vulnerabilities early and ensure secure cloud infrastructure deployment.

##**🔍 Security Scanning & Remediation**

The project uses Trivy to scan both Infrastructure as Code (Terraform) and Docker container images to identify security vulnerabilities before deployment.

###**Key Security Improvements Implemented**
####**🔐 Restricted SSH Access**

Issue: Security group allowed SSH access from anywhere (0.0.0.0/0), increasing the risk of brute-force attacks.

Solution:
SSH access restricted to trusted IP ranges to minimize unauthorized access.

####**🧾 Enforced IMDSv2**

Issue: EC2 instances using IMDSv1 could expose IAM credentials via SSRF attacks.

Solution:
Enabled Instance Metadata Service Version 2 (IMDSv2) to ensure token-based authentication.

####**💾 Encrypted EBS Volumes**

Issue: Unencrypted EBS root volumes expose data at rest.

Solution:
Enabled EBS encryption using AES-256 for improved data protection.

####**🔒 Secure Container Images**

Issue: Docker images may contain vulnerable packages.

Solution:
Trivy scans container images during the Jenkins pipeline to detect vulnerabilities before pushing images.

##**🛠️ Tools & Technologies Used**

| Category | Tools |
|----------|------|
| Cloud Platform | AWS (EC2, VPC, Security Groups) |
| Infrastructure as Code | Terraform |
| Containerization | Docker |
| CI/CD | Jenkins |
| Security Scanning | Trivy |
| Version Control | Git & GitHub |
| Operating System | Linux / Ubuntu |

##**🤖 Generative AI Usage**

Generative AI was used to support several aspects of the project:

Assisted with troubleshooting Jenkins pipeline errors

Provided guidance for Terraform configuration and AWS setup

Helped interpret Trivy vulnerability scan reports

Assisted in structuring the project documentation

Provided suggestions for DevSecOps best practices

**AI Usage Link:-** https://docs.google.com/document/d/1cSqr2Cn_DeB6DZkYzi1QSgufwWk0x0eq2g4hLMYO1SM/edit?usp=sharing

##**🚀 CI/CD Pipeline Workflow**

The Jenkins pipeline automates the entire DevSecOps process:

1️⃣ Pull code from GitHub repository
2️⃣ Build Docker image
3️⃣ Perform Trivy container scan
4️⃣ Push Docker image to registry
5️⃣ Run Terraform plan and apply
6️⃣ Deploy infrastructure on AWS
7️⃣ Run the application on an EC2 instance

##**📸 Pipeline Execution Evidence**
