---
title: "Dọn dẹp tài nguyên"
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

## Dọn dẹp các tài nguyên AWS

Chúng ta sẽ thực hiện dọn dẹp các tài nguyên AWS theo thứ tự sau:

---

### A. Xóa tài nguyên Database

#### 1. Xóa Database

1. Truy cập vào **Database instance**.
2. Chọn **Actions** → **Delete**.

   ![alt text](image.png)

3. Xác nhận thao tác xóa.

   ![alt text](image-1.png)

#### 2. Xóa Snapshot

1. Trong menu điều hướng bên trái, chọn tab **Snapshots**.
2. Chọn snapshot instance cần xóa.
3. Nhấn **Actions** → **Delete snapshot**.

   ![alt text](image-3.png)

4. Xác nhận thao tác **Xóa**.

   ![alt text](image-4.png)

#### 3. Xóa Security Group của RDS

1. Truy cập dịch vụ **EC2** → chọn **Security Groups**.
2. Chọn Security Group được tạo riêng cho RDS.
3. Nhấn **Actions** → **Delete security groups**.

   ![alt text](image-2.png)

#### 4. Xóa AWS Backup

1. Truy cập dịch vụ **AWS Backup** → chọn **Backup plans**.
2. Chọn Backup plan được tạo riêng cho RDS.
3. Chọn **Delete** để xóa

![alt text](image-15.png)

---

### B. Xóa tài nguyên Elastic Beanstalk

#### 1. Xóa IAM Role

_(Thực hiện thủ công theo yêu cầu nếu có IAM role liên quan đến Elastic Beanstalk.)_

#### 2. Xóa Elastic Beanstalk Application

1. Truy cập dịch vụ **Elastic Beanstalk**, chọn mục **Applications**.
2. Chọn ứng dụng cần xóa, sau đó nhấn **Actions** → **Delete application**.

   ![alt text](image-5.png)

3. Xác nhận thao tác xóa.

   ![alt text](image-6.png)

#### 3. Xóa Security Group của Elastic Beanstalk

1. Truy cập **EC2** → chọn **Security Groups**.
2. Chọn Security Group đã tạo riêng cho môi trường Elastic Beanstalk.
3. Nhấn **Actions** → **Delete security groups**.

   ![alt text](image-7.png)

---

### C. Xóa tài nguyên S3 và CloudFront

#### 1. Xóa S3 Bucket lưu web tĩnh

1. Truy cập dịch vụ **S3**.
2. Chọn **S3 Bucket** đang chứa tài nguyên web tĩnh.
3. Nhấn **Empty bucket** để xóa toàn bộ dữ liệu trong bucket.

   ![alt text](image-9.png)

4. Xác nhận thao tác xóa dữ liệu.

   ![alt text](image-10.png)

5. Thực hiện xóa bucket.

   ![alt text](image-11.png)

6. Xác nhận thao tác xóa bucket.

   ![alt text](image-12.png)

👉 Lặp lại các bước trên để xóa S3 bucket dùng để lưu trữ hình ảnh.

#### 2. Xóa CloudFront Distribution

1. Truy cập dịch vụ **CloudFront**.
2. Chọn **Distribution** cần xóa → nhấn **Disable**.

   ![alt text](image-13.png)

3. Sau một khoảng thời gian chờ đợi (khi trạng thái đã chuyển sang "Disabled"), nhấn **Delete** để xóa distribution.

   ![alt text](image-14.png)

✅ Như vậy, chúng ta đã hoàn tất việc dọn dẹp tài nguyên.
