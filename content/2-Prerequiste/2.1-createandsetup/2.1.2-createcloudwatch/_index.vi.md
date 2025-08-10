---
title : "Tạo CloudWatch"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Tạo Dashboard trong CloudWatch

1. Click **Dashboard.**

![VPC](/images/2.prerequisite/011-createcloud.png)

2. Click **Create dashboard.**

![VPC](/images/2.prerequisite/012-createcloud.png)

3. Đặt tên tùy chọn sau đó nhấn **Create dashboard.**

![VPC](/images/2.prerequisite/013-createcloud.png)

4. Click chọn **Line**.
  + Click **Next**.

![VPC](/images/2.prerequisite/014-createcloud.png)

5. Tại trang **Add metric graph.**
  + Click **RDS**.
  + Click **DBInstanceIdentifier.**
  + Tìm và chọn các metrics sau : **DatabaseConnections**, **FreeStorageSpace**, **ReadIOPS**, **WriteIOPS.**
  + Click **Create widget.**

![VPC](/images/2.prerequisite/015-createcloud.png)