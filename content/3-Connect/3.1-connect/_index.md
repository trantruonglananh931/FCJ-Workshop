---
title : "Connect to RDS"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---

1. Go to the [RDS service management console](https://console.aws.amazon.com/rds/)  
  + Click **Databases**.  
  + Select the database you created.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. In the **Connectivity & security** section:  
  + Save the **Endpoint** address.

![VPC](/images/3.connect/001-connects.png)

3. Open a terminal or tools such as MySQL Workbench, DBeaver  
  + Run the command: **mysql -h endpoint -P 3306 -u username -p**.  
  + Replace `endpoint` with the saved endpoint address, and `username` with the username you created for RDS.  
  + Then enter the password.

![VPC](/images/3.connect/002-connects.png)
