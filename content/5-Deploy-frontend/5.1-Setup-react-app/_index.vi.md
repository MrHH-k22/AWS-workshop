---
title: "Triển khai React web app"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 5.1 </b> "
---

## Clone react app về

1. clone github respository này về với đường dẫn sau:

   ```
   git clone https://github.com/MrHH-k22/jobseeker-frontend.git
   ```

2. Điều hướng đến thư mục của respository này

   ```
   cd jobseeker-frontend
   ```

3. Chạy câu lệnh sau để cài đặt tất cả các thư viện cho dự án.

   ```
   npm install
   ```

4. Thêm biến môi trường

- Vào file .env.production để cập nhật đường dẫn cho aws beanstalk và s3 bucket cho việc xử lý hình ảnh.

![alt text](image-1.png)

5. Chạy câu lệnh sau để biên dịch mã nguồn app thành các mã HTML/CSS/JS tĩnh để chuẩn bị deploy lên server.

- ```
  npm run build
  ```

6. Sau khi build thành công, một thư mục có tên dist sẽ được tạo ra, thư mục này chứa toàn bộ mã tĩnh của ứng dụng.

![alt text](image.png)

-> Các file tĩnh trong thư mục này sẽ được sử dụng để triển khai lên AWS S3.
