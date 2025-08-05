---
title: "Cách lưu trữ S3 trong backend"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 4.2 </b> "
---

<div style="border-left: 5px solid #1E90FF; background-color: #e6f2ff; padding: 1em; margin: 1em 0;">
<strong>📝 Lưu ý:</strong><br>
Trong phần này, chúng ta chỉ review code để hiểu cách thức lưu trữ file lên Amazon S3. Không cần chỉnh sửa gì.
</div>

## Review code S3 trong backend

- Mở project `jobseeker_backend`
- Chúng ta sẽ xem xét 2 file chính:
  - `controller/FileController.java` - xử lý API upload file
  - `service/FileService.java` - logic lưu trữ lên S3

### 1. Phân tích FileController.java

Truy cập file `controller/FileController.java` để xem API endpoint xử lý upload file:

```java
@PostMapping("/files")
@ApiMessage("upload a single file")
public ResponseEntity<ResUploadFileDTO> upload(
        @RequestParam(name = "file", required = false) MultipartFile file,
        @RequestParam("folder") String folder) throws IOException, StorageException {

    // validate
    if (file == null || file.isEmpty()) {
        throw new StorageException("File is empty. Please upload a file");
    }

    String fileName = file.getOriginalFilename();
    List<String> allowedExtensions = Arrays.asList("pdf", "jpg", "jpeg", "png", "doc", "docx");
    boolean isValid = allowedExtensions.stream()
            .anyMatch(item -> fileName.toLowerCase().endsWith(item));

    if (!isValid) {
        throw new StorageException(
                "File type is not supported. Please upload a file with one of the following extensions: "
                        + allowedExtensions);
    }

    String uploadKey = this.fileService.store(file, folder);

    ResUploadFileDTO res = new ResUploadFileDTO(uploadKey, Instant.now());
    return ResponseEntity.ok().body(res);
}
```

#### Quy trình xử lý của API:

1. **Nhận dữ liệu**: Nhận file từ request và tên thư mục đích
2. **Validation**:
   - Kiểm tra file có tồn tại và không rỗng
   - Kiểm tra định dạng file (chỉ cho phép: pdf, jpg, jpeg, png, doc, docx)
3. **Lưu trữ**: Gọi **fileService.store()** để upload file lên S3
4. **Phản hồi**: Trả về thông tin file đã upload thành công

### 2. Phân tích FileService.java

Truy cập file `service/FileService.java` để xem nghiệp vụ tương tác với Amazon S3 để lưu trữ file.

#### 2.1. Cấu hình S3

```java
@Value("${aws.s3.bucket}")
private String bucket;

@Value("${aws.s3.region}")
private String region;

@Value("${aws.s3.base-folder}")
private String baseFolder;
```

**Giải thích các tham số:**

- `bucket`: Tên S3 bucket nơi lưu trữ file
- `region`: Khu vực AWS (ví dụ: "ap-southeast-1")
- `baseFolder`: Thư mục gốc trong bucket để tổ chức file

#### 2.2. Phương thức store()

```java
public String store(MultipartFile file, String folder) throws IOException {
    String fileName = System.currentTimeMillis() + "-" + file.getOriginalFilename();
    String key = (baseFolder != null ? baseFolder : "") +
                 (folder != null ? folder + "/" : "") + fileName;

    PutObjectRequest putOb = PutObjectRequest.builder()
            .bucket(bucket)
            .key(key)
            .contentType(file.getContentType())
            .build();

    getS3Client().putObject(putOb,
            software.amazon.awssdk.core.sync.RequestBody.fromBytes(file.getBytes()));

    return key;
}
```

#### Quy trình lưu trữ:

1. Nhận file và tên thư mục cần lưu.
2. Tạo tên file duy nhất bằng cách thêm timestamp vào trước tên gốc.
3. Tạo **key** đại diện cho đường dẫn đầy đủ trong bucket.
4. Tạo **PutObjectRequest** để cấu hình thông tin cần thiết khi upload.
5. Sử dụng S3Client để upload file thông qua **putObject(...)**.
6. Trả về key để có thể sử dụng sau này.
