---
title: "Kiểm tra lưu trữ hình ảnh"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 6.2 </b> "
---

## Tạo một Company mới

1. Truy cập vào **Dashboard**, chọn tab **Company**.
2. Nhấn vào nút **Thêm mới**.
3. Nhập đầy đủ thông tin công ty và chọn hình ảnh, sau đó bấm **Tạo mới**.

   ![alt text](image.png)

4. Sau khi tạo thành công, thông tin công ty sẽ được hiển thị:

   ![alt text](image-1.png)

5. Quay lại trang chủ, bạn sẽ thấy công ty vừa tạo đã xuất hiện.

   ![alt text](image-7.png)

---

### Kiểm tra trên AWS S3

- Truy cập vào S3 Bucket để kiểm tra xem hình ảnh đã được lưu trữ thành công hay chưa.

  ![alt text](image-2.png)

✅ Hình ảnh đã được lưu trữ thành công trên S3.

---

### Kiểm tra trong cơ sở dữ liệu

- Trong bảng **Company**, dữ liệu được lưu kèm theo đường dẫn URL trỏ tới file hình ảnh trên S3 Bucket.

  ![alt text](image-3.png)

---

✅ Như vậy, chúng ta đã kiểm tra thành công tính năng lưu trữ hình ảnh trong dự án.

<div style="border-left: 5px solid #1E90FF; background-color: #e6f2ff; padding: 1em; margin: 1em 0;">
<strong>Note:</strong><br>
Các tính năng khác cũng sẽ được thực hiện và kiểm tra tương tự.
</div>
