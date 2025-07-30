---
title: "Xây dựng & triển khai Frontend tĩnh"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

## Tổng quan

Trong phần này, chúng ta sẽ xây dựng và triển khai ứng dụng frontend React lên **Amazon S3** và sử dụng **CloudFront** để phân phối nội dung. Việc sử dụng S3 và CloudFront giúp tối ưu hóa hiệu suất, giảm độ trễ và cung cấp trải nghiệm người dùng tốt hơn thông qua CDN toàn cầu.

### Mục tiêu

- Chuẩn bị và build ứng dụng React thành static files
- Cấu hình S3 bucket để host static website
- Thiết lập CloudFront distribution để tăng tốc độ truy cập
- Kết nối frontend với backend API đã triển khai

### Nội dung

1. [**Chuẩn bị React App**](5.1-setup-react-app/) - Clone, cấu hình và build ứng dụng React
2. [**Tạo S3 cho Static Website**](5.2-deploy-to-s3/) - Tạo và cấu hình S3 bucket để host static website
3. [**Triển khai CloudFront**](5.3-cloudfront/) - Thiết lập CloudFront distribution cho CDN
4. [**Sửa lỗi CORS**](5.4-fix-cors/) - Sửa lỗi CORS

---
