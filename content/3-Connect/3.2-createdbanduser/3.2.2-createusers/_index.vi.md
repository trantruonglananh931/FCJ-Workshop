---
title : "Tạo Users"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 3.2.2 </b> "
---


#### Tạo Users để phân quyền trong database

- Chúng ta sẽ tạo 2 users:
  - admin
  - auditor

1. Tạo 2 users là **admin1** và **auditor**
 + Sử dụng lệnh **create user'admin1'@'%' IDENTIFIED BY 'admin1';** để tạo user admin1.
 + Sử dụng lệnh **create user'auditor'@'%' IDENTIFIED BY 'auditor';** để tạo user auditor.

![Connect](/images/3.connect/006-createusers.png)

2. Gán quyền cho user.
  + Gán cho admin1 quyền đọc và thêm : **GRANT SELECT, INSERT ON workshop_db.* TO 'admin1'@'%';**
  + Gán cho auditor quyền ghi : **GRANT SELECT ON workshop_db.* TO 'auditor'@'%';**

![Connect](/images/3.connect/007-createusers.png)
