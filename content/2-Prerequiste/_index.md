---
title: "Prerequisites"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## A. AWS Account and Permissions

An AWS account with full access to the following services:

- **Amazon S3** (Simple Storage Service)
- **Amazon RDS** (Relational Database Service)
- **AWS Elastic Beanstalk**
- **Amazon CloudFront**
- **AWS IAM** (Identity and Access Management)
- **Amazon VPC** (Virtual Private Cloud)
- **Amazon EC2** (Elastic Compute Cloud)

**Recommendation**: Use the AWS root account for full access.

## B. Development Environment

- **Node.js** (version 16 or higher)
- **npm** or **yarn** package manager
- **Git** to clone repositories
- A text editor (VS Code, IntelliJ, etc.)
- **Java JDK 17** or later
- Java-supporting IDE (IntelliJ IDEA, Eclipse, etc.)

---

## C. Basic Knowledge Required

Basic understanding of core AWS services:

- S3 buckets and bucket policies
- RDS and MySQL database
- Elastic Beanstalk deployment
- CloudFront distribution
- IAM roles and policies

---

## D. Preparations Before Starting

### 1. Required Repositories

- Access to the following GitHub repositories:
  - Frontend: `https://github.com/MrHH-k22/jobseeker-frontend.git`
  - Backend: `https://github.com/MrHH-k22/jobseeker-backend.git`

### 2. Information to Prepare

- Prepare and note down the following:
  - Names of S3 buckets
  - Database credentials
  - AWS region to be used (recommended: `ap-southeast-1`)
  - Endpoint URLs

---

## E. Estimated Cost

⚠️ **Important Note**: This workshop uses AWS services that may incur charges:

- **RDS MySQL**: ~$15–25/month (if not using Free Tier)
- **Elastic Beanstalk**: Free (you only pay for the EC2 instance)
- **S3**: ~$1–5/month depending on usage
- **CloudFront**: ~$1–10/month depending on traffic

**Recommendation**: Perform resource cleanup after completing the workshop to avoid unexpected charges.

---

✅ **Once you have completed all the above preparations, you can proceed with the next steps of the workshop.**
