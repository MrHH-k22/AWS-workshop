---
title: "Connect to MySQL Workbench"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Connect to MySQL Workbench

In MySQL Workbench, create a new connection by selecting **MySQL Connections** > **+ (Add Connection)**.

![alt text](image.png)

### Enter the following connection details:

- **Hostname**: your database endpoint (provided during RDS creation)
- **Username**: database username (`admin`)
- **Password**: database password (`Admin2025`)

![alt text](image-2.png)

After entering the information, click on the newly created connection to initiate it:

![alt text](<image (2).png>)

✅ **Connection successful** if no errors occur and the database interface is displayed.

## Create a new schema in MySQL Workbench

1. Right-click and select **Create Schema..**

![alt text](image-1.png)

2. Enter schema name: **jobseeker-db**
3. Click **Apply**

![alt text](image-3.png)

> ⚠️ Save this schema name for use in the backend configuration later.
