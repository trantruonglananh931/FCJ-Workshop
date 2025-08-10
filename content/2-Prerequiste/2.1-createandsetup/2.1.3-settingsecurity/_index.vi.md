---
title : "Sửa Security group"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.1.3 </b> "
---

#### Sửa Security group

Trong bước này chúng ta sẽ tiến hành sữa Security group để có thể kết nối bằng máy cá nhân.

1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Click **Database**.
  + Chọn vào Database đã tạo.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. Kéo xuống **Security group rules**.
  + Click **default (sg-0c641337c0b362188).**

![VPC](/images/2.prerequisite/016-security.png)

3. Tại trang **EC2 Console**.
  + Click **sg-0c641337c0b362188**.

![VPC](/images/2.prerequisite/018-security.png)

4. Click **Edit inbound rules**.

![VPC](/images/2.prerequisite/019-security.png)

5. Click **Delete** sau đó click **Add rule**
  + Chỉnh Type thành **MySQL/Aurora** và Source thành **MyIP**.
  + Click **Save rules**.

![VPC](/images/2.prerequisite/020-security.png)