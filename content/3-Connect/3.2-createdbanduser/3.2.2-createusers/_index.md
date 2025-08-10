---
title : "Create Users"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 3.2.2 </b> "
---

#### Create Users for permission management in the database

- We will create 2 users:
  - admin
  - auditor

1. Create two users: **admin1** and **auditor**
 + Use the command **CREATE USER 'admin1'@'%' IDENTIFIED BY 'admin1';** to create the admin1 user.
 + Use the command **CREATE USER 'auditor'@'%' IDENTIFIED BY 'auditor';** to create the auditor user.

![Connect](/images/3.connect/006-createusers.png)

2. Assign permissions to the users.
  + Grant **admin1** read and insert permissions:  
    **GRANT SELECT, INSERT ON workshop_db.* TO 'admin1'@'%';**
  + Grant **auditor** read-only permissions:  
    **GRANT SELECT ON workshop_db.* TO 'auditor'@'%';**

![Connect](/images/3.connect/007-createusers.png)
