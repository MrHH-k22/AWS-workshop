---
title: "Bật Tính năng sao lưu dữ liệu cho AWS RDS"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 3.4 </b> "
---

## Tạo AWS Backup

### 🔹 Bước 1: Truy cập dịch vụ AWS Backup

1. Mở **AWS Management Console** tại: [https://aws.amazon.com/](https://aws.amazon.com/)
2. Tìm kiếm và chọn dịch vụ **AWS Backup**.

![alt text](image.png)

---

### 🔹 Bước 2: Tạo Backup Plan

3. Chọn mục **Backup plans** → nhấn **Create backup plan**.
4. Cấu hình kế hoạch sao lưu như sau:

   - **Backup plan options**: Build a new plan
   - **Backup plan name**: `jobseeker-db-weekly`
   - **Backup rule name**: `weekly-rule`
   - **Backup vault**: Default
   - **Backup frequency**: Weekly
   - Các mục còn lại giữ nguyên mặc định.

![alt text](image-1.png)

5. Nhấn **Create plan** để tạo kế hoạch sao lưu.

---

### 🔹 Bước 3: Gán tài nguyên cần sao lưu

6. Cấu hình phần **Assign resources**:

   - **Resource assignment name**: `assign-rds`
   - **IAM role**: Default role
   - **Define resource selection**: Chọn _Include specific resource types_
   - **Select specific resource types**: Chọn _RDS_
   - **Database names**: Chọn `jobseeker-db`

7. Nhấn **Assign resources** để hoàn tất.

---

### Kết quả sau khi tạo AWS Backup

![alt text](image-2.png)

✅ Bạn đã hoàn tất việc thiết lập AWS Backup để sao lưu và phục hồi cơ sở dữ liệu RDS theo lịch hàng tuần một cách tự động.
