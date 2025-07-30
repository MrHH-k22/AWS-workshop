---
title: "Create RDS Instance (MySQL)"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

## Create a New Database with Amazon RDS

1. Go to the **AWS Management Console** at [https://aws.amazon.com/](https://aws.amazon.com/)

2. Search for and select the **RDS** or **Aurora and RDS** service.

![alt text](image.png)

3. Click the **Create a database** button.

![alt text](createadatabase.png)

4. In the **Create database** section, configure the following settings:

   - **Database creation method**: `Standard Create`
   - **Engine type**: `MySQL`
   - **Engine version**: `8.0.41`
   - **RDS Extended Support**: **Off**

![alt text](image-1.png)

5. **Template** and **Availability & Durability**:

   - Leave as default (Free Tier will be used)

![alt text](image-2.png)

6. **Settings**:

   - **DB instance identifier**: `jobseeker-db`
   - **Master username**: `admin`
   - **Credential management**: `Self-managed`
   - **Master password**: `Admin2025` (or a stronger password of your choice)

> ⚠️ Remember this information — it will be needed during backend configuration.

![alt text](image-3.png)

7. **Instance Configuration** and **Storage**:

   - Keep the default settings
   - You may reduce the allocated storage to **20 GB** as the lab does not require much

![alt text](image-4.png)

8. **Connectivity**:

   - **VPC**: Select the **default VPC**
   - **Security group**: Select the **Security Group created in the previous step**
   - **Public access**: Select **Yes**
   - Leave the remaining settings as default

![alt text](image-5.png)

9. Click **Create Database** to start the process.

---

### Result After Database Creation:

![alt text](image-6.png)

> ⚠️ Save the database endpoint — you will need it when configuring the backend.
