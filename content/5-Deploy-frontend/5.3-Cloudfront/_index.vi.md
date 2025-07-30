---
title: "Phân phối nội dung web tĩnh với CloudFront"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 5.3 </b> "
---

## A. Tạo AWS CloudFront

1. Truy cập **AWS Management Console** tại [https://aws.amazon.com/](https://aws.amazon.com/).

2. Tìm kiếm và chọn dịch vụ **CloudFront**.

   ![alt text](image.png)

3. Trong mục **Distributions**, nhấn **Create Distributions**.

---

### Bước 1: Khởi tạo Distribution

- Nhập tên Distribution: **jobseeker-frontend**

  ![alt text](image-1.png)

---

### Bước 2: Cấu hình Origin

![alt text](image-2.png)

- Chọn **Origin type**: `Amazon S3`
- Trong phần **S3 origin**, chọn **Browse S3**.

  - Tick chọn **Allow private S3 bucket access to CloudFront**
  - Chọn S3 bucket đã tạo từ trước

  ![alt text](image-3.png)

- Sau khi chọn xong, AWS có thể gợi ý sử dụng **website endpoint** do bucket đã bật tính năng lưu trữ web tĩnh.

  ➤ Nhấn **Use website endpoint** để cập nhật endpoint:

  ![alt text](image-4.png)

- Kết quả S3 endpoint sau khi chọn:

  ![alt text](image-5.png)

> 📌 **Lưu ý:** Nếu AWS không hiển thị gợi ý, bạn có thể tự nhập endpoint theo cấu trúc sau:

```bash
http://{bucket-name}.s3-website.{region}.amazonaws.com
```

---

### Bước 5: Thiết lập bảo mật (Enable Security)

- Chọn: **Do not enable security protections**

  ![alt text](image-6.png)

- Sau đó, kiểm tra lại toàn bộ cấu hình và nhấn **Create distribution** để hoàn tất quá trình tạo.

---

## D. Kết quả sau khi triển khai CloudFront

![alt text](image-7.png)

---

## E. Cấu hình lại Behaviour cho CloudFront

1. Chuyển sang tab **Behaviours**
2. Chọn một behaviour và nhấn **Edit**

   ![alt text](image-8.png)

3. Chỉnh sửa các mục sau:

   - **Viewer protocol policy**: `HTTP and HTTPS`
   - **Allowed HTTP methods**: `GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE`

   ![alt text](image-9.png)

4. Các mục còn lại giữ nguyên → nhấn **Save Changes** để lưu lại cấu hình.

---

## F. Kiểm tra CloudFront Endpoint

- Sao chép **Distribution domain name** và dán vào trình duyệt để kiểm tra kết quả.

  ![alt text](image-10.png)

- Giao diện website sau khi phân phối thành công:

  ![alt text](image-11.png)

---

✅ Như vậy, bạn đã hoàn tất việc phân phối nội dung web tĩnh thông qua **Amazon CloudFront** một cách hiệu quả.
