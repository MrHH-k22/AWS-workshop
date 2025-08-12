---
title: "Thiết kế cơ sở dữ liệu sử dụng AWS RDS"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

## Tổng quan

Trong phần này, chúng ta sẽ thiết kế và triển khai cơ sở dữ liệu cho ứng dụng JobSeeker sử dụng dịch vụ **Amazon RDS (Relational Database Service)**. Cơ sở dữ liệu đóng vai trò quan trọng trong việc lưu trữ và quản lý dữ liệu nghiệp vụ của ứng dụng.

### Mục tiêu

- Tạo và cấu hình Security Group cho database để đảm bảo tính bảo mật
- Triển khai instance MySQL trên Amazon RDS với cấu hình phù hợp
- Thiết lập kết nối và chuẩn bị schema cho ứng dụng

### Nội dung

1. [**Thiết lập Security Group cho Database**](3.1-security-group/) - Tạo và cấu hình security group để kiểm soát truy cập đến database
2. [**Tạo Instance RDS (MySQL)**](3.2-create-rds/) - Triển khai database MySQL trên Amazon RDS
3. [**Kết nối tới MySQL Workbench**](3.3-connect/) - Thiết lập kết nối và tạo schema cho ứng dụng
4. [**Thiết lập dịch vụ AWS Backup**](3.4-aws-backup/) - Thiết lập aws backup để sao lưu dữ liệu

---
