---
title: "Set Up Security Group for Database"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

## Create a New Security Group

1. Go to the **AWS Management Console** homepage at [https://aws.amazon.com/](https://aws.amazon.com/)

2. Search for and select the **VPC** service.

![alt text](image.png)

3. In the VPC Dashboard, select **Security Groups**.

4. Click the **Create Security Group** button to create a new one.

![alt text](image-2.png)

5. In the **Basic Details** section, fill in the following information:

   - **Security group name**: `jobseeker-db`
   - **Description**: `Allow RDS port to anywhere`
   - **VPC**: Select the default VPC

![alt text](image-3.png)

6. Add a new **Inbound Rule**:

   - **Type**: `MySQL/Aurora`
   - **Source**: `Anywhere - IPv4`

![alt text](image-4.png)

> Note: Leave the **Outbound Rules** as default.

7. Click **Create Security Group** to finish.

---

### Result After Successfully Creating the Security Group:

![alt text](image-5.png)
