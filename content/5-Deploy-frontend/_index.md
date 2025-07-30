---
title: "Build & Deploy Static Frontend"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

## Overview

In this section, we will build and deploy a React frontend application to **Amazon S3** and use **CloudFront** for content distribution. Using S3 and CloudFront helps optimize performance, reduce latency, and provide a better user experience through a global CDN.

### Objectives

- Prepare and build the React application into static files
- Configure S3 bucket to host static website
- Set up CloudFront distribution to accelerate access speed
- Connect frontend with the deployed backend API

### Contents

1. [**Prepare React App**](5.1-setup-react-app/) - Clone, configure and build the React application
2. [**Create S3 for Static Website**](5.2-deploy-to-s3/) - Create and configure S3 bucket to host static website
3. [**Deploy CloudFront**](5.3-cloudfront/) - Set up CloudFront distribution for CDN
4. [**Fix CORS Error**](5.4-fix-cors/) - Fix CORS error

---
