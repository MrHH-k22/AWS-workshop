# Workshop: Triển khai Ứng dụng Web với AWS Elastic Beanstalk, S3, RDS và CloudFront

## Tổng quan Workshop

Workshop này hướng dẫn bạn xây dựng và triển khai một ứng dụng web hoàn chỉnh trên nền tảng AWS. Bạn sẽ thực hành từng bước từ thiết kế cơ sở dữ liệu, triển khai backend (Spring Boot), xây dựng frontend tĩnh, đến tối ưu hóa và bảo mật hệ thống với các dịch vụ chủ chốt của AWS. Mục tiêu là giúp bạn làm quen với quy trình triển khai thực tế trên cloud, quản lý tài nguyên hiệu quả và đảm bảo bảo mật, hiệu năng cho ứng dụng.

## Kỹ thuật sử dụng

- **Java Spring Boot**: Xây dựng backend RESTful API, xử lý nghiệp vụ, xác thực JWT.
- **MySQL**: Lưu trữ dữ liệu nghiệp vụ trên Amazon RDS.
- **Frontend tĩnh**: Được lưu trữ trên Amazon S3 và phân phối qua CloudFront.
- **AWS IAM**: Quản lý quyền truy cập tài nguyên.
- **CI/CD thủ công**: Build, upload và deploy ứng dụng qua AWS Console.

## Dịch vụ AWS sử dụng

- **Amazon S3**: Lưu trữ website tĩnh, hình ảnh, file upload.
- **Amazon RDS**: Quản lý cơ sở dữ liệu MySQL.
- **AWS Elastic Beanstalk**: Triển khai và quản lý backend Spring Boot.
- **Amazon CloudFront**: Phân phối nội dung tĩnh, tăng tốc truy cập.
- **AWS IAM**: Quản lý quyền truy cập và bảo mật.
- **Amazon VPC & EC2**: Quản lý mạng, máy chủ và bảo mật.
- **AWS Backup**: Sao lưu dữ liệu tự động.

## Cách chạy Workshop với Hugo

1. **Cài đặt Hugo**

   - Tải và cài đặt Hugo: [https://gohugo.io/getting-started/installing/](https://gohugo.io/getting-started/installing/)
   - Kiểm tra cài đặt:
     ```
     hugo version
     ```

2. **Clone source code workshop**

   ```
   git clone https://github.com/MrHH-k22/AWS-workshop
   cd AWS-workshop
   ```

3. **Chạy server Hugo để xem tài liệu**
   ```
   hugo server
   ```
   - Truy cập trình duyệt tại địa chỉ: [http://localhost:1313](http://localhost:1313)
