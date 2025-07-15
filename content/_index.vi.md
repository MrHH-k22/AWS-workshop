---
title: "Session Management"
date: "`r Sys.Date()`"
weight: 1
chapter: false
---

# Thiết kế hệ thống web app không Server

### Tổng quan

Trong bài lab này, bạn sẽ được học cách xây dựng một ứng dụng web serverless trên AWS một cách thực tế, tập trung vào việc thực hành với các dịch vụ AWS đa dạng. Bạn sẽ được học cách sử dụng các dịch vụ như Amazon Cognito - Xác thực và ủy quyền người dùng, Amazon S3 - lưu trữ website tĩnh, Amazon API Gateway - tạo và quản lý API, AWS Lambda - xử lý logic nghiệp vụ, Amazon DynamoDB - lưu trữ dữ liệu NoSQL. Mục tiêu workshop là giúp bạn nắm bắt cách tạo ứng dụng không cần quản lý server, chỉ tính phí theo sử dụng.

![ConnectPrivate](/images/AWS.jpg)

### Chi phí ước tính

Chi phí ước tính cho workshop này là **0 đồng**, vì chúng ta sẽ sử dụng AWS Free Tier trong 12 tháng đầu tiên khi tạo tài khoản mới, cho phép truy cập miễn phí vào các dịch vụ cơ bản mà không phát sinh phí.

### Thời gian hoàn thành ước tính

Workshop được thiết kế ngắn gọn, kéo dài khoảng **2-3 giờ**, với các phần thực hành trực tiếp trên AWS Console.

1. Giới thiệu (15 phút): Khái niệm serverless và thiết lập tài khoản AWS.

2. Thiết kế Kiến trúc (20 phút): Vẽ sơ đồ tổng thể (frontend từ S3, backend qua Lambda và API Gateway).

3. Thực hành Triển khai (60-90 phút): Bước từng bước build ứng dụng, từ tạo Lambda function đến tích hợp DynamoDB và deploy.

4. Kết thúc (15 phút): Thảo luận best practices, Q&A, và cách scale lên.

### Nội dung

1.  [Giới thiệu](1-introduce/)
2.  [Các bước chuẩn bị](2-Prerequiste/)
3.  [Tạo kết nối đến máy chủ EC2](3-Accessibilitytoinstance/)
4.  [Quản lý session logs](4-s3log/)
5.  [Port Forwarding](5-Portfwd/)
6.  [Dọn dẹp tài nguyên](6-cleanup/)
