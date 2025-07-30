---
title: "Yêu cầu tiên quyết"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## A. Tài khoản và quyền truy cập

Tài khoản AWS có đầy đủ quyền truy cập các dịch vụ:

- **Amazon S3** (Simple Storage Service)
- **Amazon RDS** (Relational Database Service)
- **AWS Elastic Beanstalk**
- **Amazon CloudFront**
- **AWS IAM** (Identity and Access Management)
- **Amazon VPC** (Virtual Private Cloud)
- **Amazon EC2** (Elastic Compute Cloud)

**Khuyến nghị**: Tạo và sử dụng tải khoản AWS root

## B. Môi trường phát triển

- **Node.js** (phiên bản 16 trở lên)
- **npm** hoặc **yarn** package manager
- **Git** để clone repository
- Text editor (VS Code, IntelliJ, v.v.)
- **Java JDK 17** trở lên
- IDE hỗ trợ Java (IntelliJ IDEA, Eclipse, v.v.)

---

## C. Kiến thức cơ bản

Hiểu biết cơ bản về các dịch vụ AWS core:

- S3 buckets và bucket policies
- RDS và MySQL database
- Elastic Beanstalk deployment
- CloudFront distribution
- IAM roles và policies

---

## D. Chuẩn bị trước khi bắt đầu

### 1. Repository cần thiết

- Truy cập được các GitHub repositories:
  - Frontend: `https://github.com/MrHH-k22/jobseeker-frontend.git`
  - Backend: `https://github.com/MrHH-k22/jobseeker-backend.git`

### 2. Chuẩn bị thông tin

- Ghi chú sẵn các thông tin sẽ cần dùng:
  - Tên các S3 buckets
  - Database credentials
  - Region sử dụng (khuyến nghị: `ap-southeast-1`)
  - Endpoint URLs

---

## E. Ước tính chi phí

⚠️ **Lưu ý quan trọng**: Workshop này sử dụng các dịch vụ AWS có thể phát sinh chi phí:

- **RDS MySQL**: ~$15-25/tháng (nếu không dùng Free Tier)
- **Elastic Beanstalk**: Miễn phí (chỉ trả phí EC2 instance)
- **S3**: ~$1-5/tháng tùy usage
- **CloudFront**: ~$1-10/tháng tùy traffic

**Khuyến nghị**: Thực hiện cleanup sau khi hoàn thành để tránh chi phí không mong muốn.

---

✅ **Sau khi đã chuẩn bị đầy đủ các yêu cầu trên, bạn có thể tiến hành các bước tiếp theo của workshop.**
