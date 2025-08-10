---
title : "Granting User Permissions for the Database"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

Both **admin1** and **auditor** users only have permissions for the **workshop_db** database.

#### Verify Database Permissions for Both Users

1. Log in with the **admin1** account.

![S3](/images/4.penetration/001-user.png)

2. View the available databases  
  + **show databases;**  
  + Only the **workshop_db** database is available.
 
![S3](/images/4.penetration/002-user.png)

3. Repeat the process with the **auditor** account  
  + The result still shows only **workshop_db**.
 
![S3](/images/4.penetration/003-user.png)

Next, we will access **workshop_db** to test with queries.
