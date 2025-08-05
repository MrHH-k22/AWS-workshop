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

1. [**Create an S3 Bucket for Images**](4.1-Image-S3-bucket/) – Create and configure an S3 bucket for file uploads
2. [**Set up Spring Boot App**](4.2-Setup-Springboot-app/) – Clone, build, and prepare the JAR file for deployment
3. [**Configure IAM Role**](4.3-Configure-IAM-role/) – Create the required IAM roles for Elastic Beanstalk
4. [**Deploy to AWS Beanstalk**](4.4-Create-beanstalk/) – Create and configure the Elastic Beanstalk environment

---
