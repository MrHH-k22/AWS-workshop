---
title: "Image Storage Testing"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 6.2 </b> "
---

## Create a New Company

1. Go to the **Dashboard** and select the **Company** tab.
2. Click the **Add New** button.
3. Fill in the company details and choose an image, then click **Create**.

   ![alt text](image.png)

4. After successful creation, the company information will be displayed:

   ![alt text](image-1.png)

5. Return to the homepage, and you'll see the newly created company listed.

   ![alt text](image-7.png)

---

### Check on AWS S3

- Go to your S3 Bucket to verify whether the image has been successfully stored.

  ![alt text](image-2.png)

✅ The image has been successfully stored on S3.

---

### Check in the Database

- In the **Company** table, the data is saved along with the image file's URL pointing to the S3 Bucket.

  ![alt text](image-3.png)

---

✅ We have successfully tested the image storage feature in the project.  
Other features will be implemented and tested in a similar manner.
