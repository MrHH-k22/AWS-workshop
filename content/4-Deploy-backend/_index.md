---
title: "Deploy Backend with AWS Beanstalk"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

## Overview

In this section, we will deploy the Java Spring Boot backend application to **AWS Elastic Beanstalk** to handle APIs and business logic. AWS Elastic Beanstalk automatically configures EC2, creates Security Groups, and manages network interfaces, simplifying the deployment process.

### Objectives

- Create an S3 Bucket to store images uploaded by users
- Prepare and build the Spring Boot application into a JAR file
- Configure the necessary IAM Roles for AWS Elastic Beanstalk
- Deploy the backend to Elastic Beanstalk with appropriate environment variables

### Content

1. [**Create an S3 Bucket for Images**](4.1-image-s3-bucket/) – Create and configure an S3 bucket for file uploads
2. [**How to store S3 in backend**](4.2-review-s3-code/) - Review S3 code to store files in backend.
3. [**Set up Spring Boot App**](4.2-setup-springboot-app/) – Clone, build, and prepare the JAR file for deployment
4. [**Configure IAM Role**](4.3-configure-iam-role/) – Create the required IAM roles for Elastic Beanstalk
5. [**Deploy to AWS Beanstalk**](4.4-create-beanstalk/) – Create and configure the Elastic Beanstalk environment

---
