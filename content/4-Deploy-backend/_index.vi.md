---
title: "Triển khai Backend với AWS Beanstalk"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

## Tổng quan

Trong phần này, chúng ta sẽ triển khai ứng dụng backend Java Spring Boot lên **AWS Elastic Beanstalk** để xử lý các API và logic nghiệp vụ. AWS Elastic Beanstalk sẽ tự động cấu hình EC2, tạo Security Group, và quản lý network interfaces, giúp đơn giản hóa quá trình triển khai.

### Mục tiêu

- Tạo S3 Bucket để lưu trữ hình ảnh upload từ người dùng
- Chuẩn bị và build ứng dụng Spring Boot thành file JAR
- Cấu hình IAM Roles cần thiết cho AWS Elastic Beanstalk
- Triển khai backend lên Elastic Beanstalk với các biến môi trường phù hợp

### Nội dung

1. [**Tạo S3 Bucket cho hình ảnh**](4.1-image-s3-bucket/) - Tạo và cấu hình S3 bucket để lưu trữ files upload
2. [**Cách lưu trữ S3 trong backend**](4.2-review-s3-code/) - Review code S3 lưu trữ file trong backend.
3. [**Thiết lập Spring Boot app**](4.2-setup-springboot-app/) - Clone, build và chuẩn bị file JAR cho deployment
4. [**Cấu hình IAM Role**](4.3-configure-iam-role/) - Tạo các IAM roles cần thiết cho Elastic Beanstalk
5. [**Triển khai AWS Beanstalk**](4.4-create-beanstalk/) - Tạo và cấu hình môi trường Elastic Beanstalk

---
