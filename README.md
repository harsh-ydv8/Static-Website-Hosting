# 🌐 Static Website Hosting using AWS CI/CD & Terraform

This project showcases an end-to-end automated deployment of a static website using AWS services, CI/CD pipelines, and Infrastructure as Code. Built as part of my DevOps internship capstone, it demonstrates real-world implementation of modern DevOps practices including Terraform provisioning, S3 hosting, GitHub integration, and AWS CodePipeline automation.

---

## 🚀 Project Overview

The primary objective was to provision AWS infrastructure and host a static HTML/CSS website on S3 with a version-controlled, CI/CD-enabled pipeline. The pipeline automatically deploys changes committed to GitHub directly to the S3 bucket via AWS CodePipeline and CodeBuild. All resources were provisioned using Terraform, enabling repeatable and consistent deployments.

---

## 🧰 Tech Stack & Tools

| Category | Tools Used |
|----------|------------|
| Cloud Provider | AWS (S3, IAM, CodePipeline, CodeBuild) |
| IaC (Infrastructure as Code) | Terraform |
| CI/CD | Jenkins, GitHub, AWS CodePipeline |
| Configuration & Orchestration | Ansible (conceptual), Shell scripting |
| Containerization | Docker |
| Version Control | Git & GitHub |
| OS Environment | Ubuntu/Linux |

---


## ⚙️ Implementation Details

### 1. **Terraform Infrastructure Setup**
- Provisioned an AWS S3 bucket with public access for static website hosting.
- Created and attached a bucket policy using `bucket-policy.json`.
- Enabled static website hosting configuration with defined `index.html` and `404.html`.
- Used Terraform scripts to manage resources including IAM roles for CodePipeline.

### 2. **Static Website Development**
- Built a basic responsive HTML/CSS-based website for demonstration.
- Uploaded all site files into the S3 bucket.

### 3. **CI/CD Automation Pipeline**
- Configured AWS CodePipeline to trigger on GitHub `main` branch pushes.
- Set up CodeBuild to pull the website source and sync it with the S3 bucket.
- Used shell scripting for deployment steps.
- Optional Jenkins pipeline created for alternate automation flow.

### 4. **Deployment Flow**
```mermaid
graph TD
    A[GitHub Push] --> B[AWS CodePipeline]
    B --> C[AWS CodeBuild]
    C --> D[S3 Bucket Deployment]
    D --> E[Website Live]
