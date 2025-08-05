---
title: "Setting up Spring Boot app"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 4.3 </b> "
---

## Clone the Spring Boot app

1. Clone this GitHub repository using the following URL:

   ```
   git clone https://github.com/MrHH-k22/jobseeker-backend.git
   ```

2. Navigate to the repository directory

   ```
   cd jobseeker-backend
   ```

3. Run the following command to package the Spring Boot app into a JAR file

- ```
  ./gradlew bootJar
  ```

4. In the repository directory, go to **build/libs/** to get the JAR file

![alt text](image.png)

-> We will use this JAR file to deploy to AWS Beanstalk
