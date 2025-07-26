---
title: "Kiến trúc hệ thống"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b> 1.3 </b>"
---

## Kiến trúc Serverless

**Kiến trúc Serverless là gì?**

Serverless không có nghĩa là không có server, mà là việc quản lý server được chuyển hoàn toàn cho **cloud provider**. Kiến trúc này mang lại nhiều lợi ích:

- ✅ Không cần quản lý hạ tầng (infrastructure)
- 🔁 Tự động scale theo nhu cầu
- 💰 Chỉ trả tiền khi sử dụng
- 🎯 Tập trung vào business logic

---

## Kiến trúc AWS

![ConnectPrivate](/images/workshop-architect.png)

Ứng dụng của chúng ta sử dụng kiến trúc **3-tier serverless** gồm:

---

### 1. Presentation Tier – Giao diện người dùng

Sử dụng các dịch vụ sau để tạo ra trang web tĩnh:

- **AWS Route 53**:  
  Quản lý DNS, giúp chuyển hướng tên miền của người dùng đến CloudFront.
- **AWS CloudFront**:  
  Phân phối nội dung tĩnh (HTML, CSS, JS) từ Amazon S3 đến người dùng.

- **AWS S3**:  
  Lưu trữ nội dung trang web tĩnh như HTML, CSS, JS, hình ảnh, v.v.

---

### 2. Application Tier – Xử lý nghiệp vụ

Sử dụng các dịch vụ AWS để xử lý business logic:

- **AWS Cognito**:  
  Cung cấp chức năng xác thực và quản lý người dùng. Sau khi đăng nhập, người dùng sẽ được cấp token để gọi API.

- **Amazon API Gateway**:  
  Là cầu nối giữa frontend và backend, cho phép gửi request thông qua các RESTful API endpoint.

- **AWS Lambda**:  
  Xử lý các logic nghiệp vụ dưới dạng hàm serverless. Có thể tương tác với S3 hoặc DynamoDB.

- **AWS IAM**:  
  Cấp quyền truy cập cho Lambda đến các dịch vụ như DynamoDB, S3, SES, v.v.

---

### 3. Data Tier – Lưu trữ dữ liệu

Sử dụng các dịch vụ sau:

- **Amazon DynamoDB**:  
  Lưu trữ toàn bộ dữ liệu ứng dụng dưới dạng NoSQL.

- **AWS S3**:  
  Lưu trữ các tệp tin như hình ảnh do người dùng tải lên.

- **AWS Backup**:  
  Tự động sao lưu dữ liệu từ DynamoDB để bảo vệ và khôi phục khi cần.

---

### 🔧 Dịch vụ AWS hỗ trợ thêm

- **Amazon SES**:  
  Gửi email thông báo đến người dùng.

- **AWS CloudWatch**:  
  Giám sát hiệu suất, ghi log và tạo cảnh báo từ các dịch vụ như Lambda, API Gateway, DynamoDB, SES.

---
