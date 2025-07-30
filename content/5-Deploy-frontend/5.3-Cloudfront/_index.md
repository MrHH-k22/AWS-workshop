---
title: "Distribute static web content with CloudFront"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 5.3 </b> "
---

## A. Create AWS CloudFront

1. Access **AWS Management Console** at [https://aws.amazon.com/](https://aws.amazon.com/).

2. Search for and select **CloudFront** service.

   ![alt text](image.png)

3. In the **Distributions** section, click **Create Distribution**.

---

### Step 1: Initialize Distribution

- Enter Distribution name: **jobseeker-frontend**

  ![alt text](image-1.png)

---

### Step 2: Configure Origin

![alt text](image-2.png)

- Select **Origin type**: `Amazon S3`
- In the **S3 origin** section, select **Browse S3**.

  - Check **Allow private S3 bucket access to CloudFront**
  - Select the S3 bucket created earlier

  ![alt text](image-3.png)

- After selection, AWS may suggest using **website endpoint** since the bucket has static web hosting enabled.

  ➤ Click **Use website endpoint** to update the endpoint:

  ![alt text](image-4.png)

- Result of S3 endpoint after selection:

  ![alt text](image-5.png)

> 📌 **Note:** If AWS doesn't show the suggestion, you can manually enter the endpoint following this structure:

```bash
http://{bucket-name}.s3-website.{region}.amazonaws.com
```

---

### Step 5: Set up Security (Enable Security)

- Select: **Do not enable security protections**

  ![alt text](image-6.png)

- Then, review all configurations and click **Create distribution** to complete the creation process.

---

## D. Result after deploying CloudFront

![alt text](image-7.png)

---

## E. Reconfigure Behaviour for CloudFront

1. Switch to the **Behaviours** tab
2. Select a behaviour and click **Edit**

   ![alt text](image-8.png)

3. Edit the following settings:

   - **Viewer protocol policy**: `HTTP and HTTPS`
   - **Allowed HTTP methods**: `GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE`

   ![alt text](image-9.png)

4. Keep other settings unchanged → click **Save Changes** to save the configuration.

---

## F. Test CloudFront Endpoint

- Copy the **Distribution domain name** and paste it into a browser to check the result.

  ![alt text](image-10.png)

- Website interface after successful distribution:

  ![alt text](image-11.png)

---

✅ You have successfully completed distributing static web content through **Amazon CloudFront** efficiently.
