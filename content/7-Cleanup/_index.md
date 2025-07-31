---
title: "Clean Up Resources"
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

## Clean Up AWS Resources

We will clean up AWS resources in the following order:

---

### A. Delete Database Resources

#### 1. Delete the Database

1. Go to **Database instance**.
2. Click **Actions** → **Delete**.

   ![alt text](image.png)

3. Confirm the delete action.

   ![alt text](image-1.png)

#### 2. Delete Snapshot

1. In the left navigation menu, go to the **Snapshots** tab.
2. Select the snapshot instance you want to delete.
3. Click **Actions** → **Delete snapshot**.

   ![alt text](image-3.png)

4. Confirm the **Delete** action.

   ![alt text](image-4.png)

#### 3. Delete RDS Security Group

1. Go to **EC2** service → select **Security Groups**.
2. Select the Security Group created specifically for RDS.
3. Click **Actions** → **Delete security groups**.

   ![alt text](image-2.png)

#### 4. Delete AWS Backup

1. Go to **AWS Backup** service → select **Backup plans**.
2. Select the Backup plan created specifically for RDS.
3. Click **Delete**

![alt text](image-15.png)

---

### B. Delete Elastic Beanstalk Resources

#### 1. Delete IAM Role

_(Manually remove if any IAM roles related to Elastic Beanstalk exist.)_

#### 2. Delete Elastic Beanstalk Application

1. Go to the **Elastic Beanstalk** service, then go to **Applications**.
2. Select the application to delete, then click **Actions** → **Delete application**.

   ![alt text](image-5.png)

3. Confirm the deletion.

   ![alt text](image-6.png)

#### 3. Delete Elastic Beanstalk Security Group

1. Go to **EC2** → select **Security Groups**.
2. Choose the Security Group created for the Elastic Beanstalk environment.
3. Click **Actions** → **Delete security groups**.

   ![alt text](image-7.png)

---

### C. Delete S3 and CloudFront Resources

#### 1. Delete S3 Bucket for Static Website

1. Go to the **S3** service.
2. Select the **S3 Bucket** that contains the static website assets.
3. Click **Empty bucket** to remove all data inside the bucket.

   ![alt text](image-9.png)

4. Confirm the data deletion.

   ![alt text](image-10.png)

5. Proceed to delete the bucket.

   ![alt text](image-11.png)

6. Confirm the bucket deletion.

   ![alt text](image-12.png)

👉 Repeat the above steps to delete the S3 bucket used for image storage.

#### 2. Delete CloudFront Distribution

1. Go to the **CloudFront** service.
2. Select the **Distribution** to be deleted → click **Disable**.

   ![alt text](image-13.png)

3. After some time (once the status changes to "Disabled"), click **Delete** to remove the distribution.

   ![alt text](image-14.png)

✅ So, we have completed the resource cleanup.
