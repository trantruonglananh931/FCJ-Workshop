---
title : "Tạo Database "
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1.1 </b> "
---


#### Tạo Database **Lab Database**
1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Click **Create Database**.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. Tại trang **Create Database**.
  + Tại mục **Choose a database creation method**, chọn **Standard create**.
  + Tại mục **Engine options**, chọn **MySQL**.
  + Bỏ chọn **Show only versions that support the Multi-AZ DB cluster** và **Show only versions that support the Amazon RDS Optimized Writes**.
  + **Engine version** sử dụng phiên bản mới nhất và bỏ chọn **Enable RDS Extended Support**.
  + Tại mục **Template**, chọn **Free Tier**.

![VPC](/images/2.prerequisite/002-createdatabase.png)
![VPC](/images/2.prerequisite/003-createdatabase.png)

3. Tại phần **Setting**.
  + Tại mục **DB instance identifier**, điền **tên database**(tự chọn).
  + Tại mục **Master username**, điền **admin**.
  + Tại mục **Credentials management**, chọn **Self managed**.
  + Tại mục **Master password**, điền **mật khẩu**.
  + Tại mục **Confirm master password**, điền lại **mật khẩu đã nhập ở trên**.

![VPC](/images/2.prerequisite/004-createdatabase.png)

4. Tại phần **Instance configuration**.
  + Chọn **db.t3.micro**.
  + Giữ nguyên phần còn lại.

![VPC](/images/2.prerequisite/005-createdatabase.png)

5. Tại phần **Storage**.
  + Click vào **Additional storage configuration**.
  + Bỏ chọn **Enable storage autoscaling**.

![VPC](/images/2.prerequisite/006-createdatabase.png)

5. Tại phần **Connectivity**.
  + Tại phần **Public access**, chọn **Yes**.
  + Giữ nguyên phần còn lại.

![VPC](/images/2.prerequisite/007-createdatabase.png)

6. Tại phần **Database authentication**.
  + Chọn **Password and IAM database authentication**.

![VPC](/images/2.prerequisite/008-createdatabase.png)

7. Tại phần **Monitoring**.
  + Tại phần **Log exports**, chọn **Audit log**, **Slow query log** và **iam-db-auth-error log**.

![VPC](/images/2.prerequisite/009-createdatabase.png)

8. Tại phần **Additional configuration**.
  + Ở mục **Initial database name**, điền **tên của database**(tự chọn).

![VPC](/images/2.prerequisite/010-createdatabase.png)

9. Kéo xuống cuối trang, click **Create database**.

