---
title : "Kết nối đến RDS"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---

1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Click **Database**.
  + Chọn vào Database đã tạo.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. Tại mục **Connectivity & security.**
  + Lưu lại địa chỉ **Endpoint**.

![VPC](/images/3.connect/001-connects.png)

3. Mở terminal hoặc các công cụ như MySQL Workbench, DBeaver
  + Gõ lệnh **mysql -h endpoint -P 3306 -u username -p**.
  + Thay endpoint bằng địa chỉ endpoint vừa lưu, username bằng username lúc tạo rds.
  + Sau đó nhập mật khẩu.

![VPC](/images/3.connect/002-connects.png)


