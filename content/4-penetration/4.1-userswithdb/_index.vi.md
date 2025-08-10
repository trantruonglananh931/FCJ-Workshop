---
title : "Phân quyền user với database"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

Cả 2 user là **admin1** và **auditor** đều chỉ có quyền với database **workshop_db**.

#### Thực hiện kiểm tra quyền database với 2 user

1. Đăng nhập bằng tài khoản **admin1**

![S3](/images/4.penetration/001-user.png)

2. Xem các database hiện có
  + **show databases;**.
  + Chỉ có database **workshop_db**.
 
![S3](/images/4.penetration/002-user.png)

3. Làm tương tự với tài khoản **auditor**
  + Kết quả vẫn chỉ có **workshop_db**.
 
![S3](/images/4.penetration/003-user.png)

Tiếp theo chúng ta sẽ truy cập vào **workshop_db** để kiểm tra với các query.