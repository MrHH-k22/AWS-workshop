---
title: "Create S3 bucket to deploy React web app"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 5.2 </b> "
---

## A. Create S3 Bucket

1. Access **AWS Management Console** at [https://aws.amazon.com/](https://aws.amazon.com/)

2. Search for and select **S3** service.

![alt text](image.png)

3. In the **General purpose buckets** section, select **Create Bucket**.

4. Name the bucket: `jobseeker-frontend`

![alt text](image-1.png)

5. In the **Block Public Access settings** section:

   - **Disable all Block Public Access options**

![alt text](image-2.png)

6. Keep all other settings as default.

7. Click **Create Bucket** to complete.

---

### Result after creating S3 Bucket:

![alt text](image-3.png)

## B. Upload static code to S3

- Click the upload button to start uploading files:
- Drag all compiled files from the previous step located in the dist folder and drop them here

![alt text](image-4.png)

- Click upload to start uploading

### Result when upload is successful:

![alt text](image-5.png)

## C. Enable S3 static website hosting feature

- 1. Go to the properties tab
- 2. Scroll down to the **Static website hosting** section
- 3. Click **Edit**

![alt text](image-6.png)

- 4. Enable **Static website hosting**

![alt text](image3.png)

- 5. Configure the following:

  - Hosting type: **Host a static website**
  - Index document: enter **index.html**
  - Error document: enter **index.html**

![alt text](image-7.png)

- 6. Click **Save changes** to save everything

## D. Set up Bucket Policy

1. Switch to the **Permissions** tab of the bucket.

2. Scroll down to the **Bucket policy** section and click **Edit**.

![alt text](image-8.png)

3. Paste the following JSON into the policy section:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::jobseeker-frontend/*"
        }
    ]
}
```

![alt text](image-9.png)

> ⚠️ If you use a different bucket name, replace `jobseeker-frontend` in the `"Resource"` section with your bucket name.

4. Click **Save** to save the policy.

---

✅ You have successfully completed deploying the React web app to an **S3 Bucket**.
