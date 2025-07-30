---
title: "Session Management"
date: "`r Sys.Date()`"
weight: 1
chapter: false
---

# Thiết kế hệ thống web app sử dụng Elastic Beanstalk và CloudFront

### Tổng quan

Trong bài lab này, bạn sẽ học cách xây dựng một ứng dụng web hoàn chỉnh trên nền tảng điện toán đám mây AWS. Bài lab tập trung vào thực hành, giúp bạn làm quen với các dịch vụ đa dạng của AWS thông qua các bước triển khai thực tế.

Cụ thể, bạn sẽ được hướng dẫn sử dụng:

- **Amazon S3**: Lưu trữ website tĩnh
- **Amazon RDS**: Lưu trữ cơ sở dữ liệu SQL
- **AWS Elastic Beanstalk**: Triển khai và mở rộng ứng dụng web
- **Amazon CloudFront**: Phân phối nội dung và bảo mật truy cập

Mục tiêu của workshop là giúp bạn hiểu cách triển khai một hệ thống ứng dụng thực tế trên môi trường đám mây.

![ConnectPrivate](/images/workshop-architect.png)

---

### Chi phí ước tính

Workshop này **không phát sinh chi phí** vì bạn sẽ sử dụng gói **AWS Free Tier** (miễn phí 12 tháng đầu cho tài khoản mới), bao gồm quyền truy cập vào các dịch vụ cơ bản của AWS.

---

### Thời gian hoàn thành ước tính

Thời lượng workshop khoảng **2–3 giờ**, bao gồm các bước thực hành trực tiếp trên AWS Console:

1. **Giới thiệu (15–20 phút)**:

   - Mục tiêu
   - Các dịch vụ AWS
   - Kiến trúc hệ thống

2. **Yêu cầu tiên quyết (5–10 phút)**:

   - Tài khoản AWS
   - IDE, môi trường phát triển

3. **Thực hành triển khai (60–90 phút)**:

   - Tạo cơ sở dữ liệu
   - Triển khai backend
   - Triển khai frontend

4. **Dọn dẹp tài nguyên (15–20 phút)**:
   - Xóa toàn bộ tài nguyên để tránh phát sinh chi phí sau khi kết thúc

---

### Nội dung

1. [Giới thiệu](1-introduce/)
2. [Yêu cầu tiên quyết](2-prerequiste/)
3. [Thiết kế cơ sở dữ liệu sử dụng AWS RDS](3-create-database/)
4. [Triển khai Backend với AWS Beanstalk](4-deploy-backend/)
5. [Xây dựng & triển khai Frontend tĩnh](5-deploy-frontend/)
6. [Kiểm tra các tính năng trong chương trình](6-testing/)
7. [Dọn dẹp tài nguyên](7-cleanup/)
