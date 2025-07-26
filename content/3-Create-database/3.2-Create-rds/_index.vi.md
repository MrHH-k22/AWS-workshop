---
title: "Tạo Instance RDS (MySQL)"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

## Tạo một Database Mới với Amazon RDS

1. Truy cập **AWS Management Console** tại [https://aws.amazon.com/](https://aws.amazon.com/)

2. Tìm kiếm và chọn dịch vụ **RDS** hoặc **Aurora and RDS**.

![alt text](image.png)

3. Nhấn nút **Create a database**.

![alt text](createadatabase.png)

4. Trong phần **Create database**, cấu hình như sau:

   - **Database creation method**: `Standard Create`
   - **Engine type**: `MySQL`
   - **Engine version**: `8.0.41`
   - **RDS Extended Support**: **Tắt**

![alt text](image-1.png)

5. **Template** và **Availability & Durability**:

   - Để mặc định vì sử dụng gói **Free tier**.

![alt text](image-2.png)

6. **Settings**:

   - **DB instance identifier**: `jobseeker-db`
   - **Master username**: `admin`
   - **Credential management**: `Self-managed`
   - **Master password**: `Admin2025` (hoặc sử dụng mật khẩu mạnh hơn)

> ⚠️ Ghi nhớ các thông tin này để sử dụng trong phần cấu hình backend sau.

![alt text](image-3.png)

7. **Instance configuration** và **Storage**:

   - Giữ các thiết lập mặc định.
   - Có thể giảm dung lượng xuống **20 GB** do bài lab không yêu cầu nhiều.

![alt text](image-4.png)

8. **Connectivity**:

   - **VPC**: Chọn **VPC mặc định**
   - **Security group**: Chọn **Security group đã tạo ở bước trước**
   - Các mục còn lại: Để mặc định

![alt text](image-5.png)

9. Nhấn **Create Database** để bắt đầu tạo.

---

### Kết quả sau khi tạo xong:

![alt text](image-6.png)

> ⚠️ Lưu database endpoint để sử dụng trong phần cấu hình backend.
