---
title: "Kết nối tới MySQL Workbench"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Kết nối tới MySQL Workbench

Trong MySQL Workbench, tạo một kết nối mới bằng cách chọn **MySQL Connections** > **+ (Add Connection)**.

![alt text](image.png)

### Nhập các thông tin kết nối như sau:

- **Connection name**: tên connection (`aws-jobseeker-db`)
- **Hostname**: endpoint của database (được cung cấp khi tạo RDS)
- **Username**: tên người dùng cơ sở dữ liệu (`admin`)
- **Password**: mật khẩu của cơ sở dữ liệu (`Admin2025`)

![alt text](image-2.png)

Sau khi nhập đầy đủ thông tin, nhấn vào kết nối vừa tạo để bắt đầu kết nối:

![alt text](<image (2).png>)

✅ **Kết nối thành công** nếu không có lỗi xảy ra và giao diện database được hiển thị.

## Tạo scheme mới trong MySQL Connection

1. Bấm chuột phải và chọn **Create Schema..**

![alt text](image-1.png)

2. Nhập tên scheme: **jobseeker-db**
3. Nhấn **apply**

![alt text](image-3.png)

> ⚠️ Lưu tên scheme này để sử dụng trong phần cấu hình backend sau.
