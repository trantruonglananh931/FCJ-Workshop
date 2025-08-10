+++
title = "Dọn dẹp tài nguyên"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này. Sử dụng tài khoản đủ quyền hoặc dùng tài khoản email root.

#### Xóa RDS

1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Truy cập vào **Databases>securedb**

![S3](/images/4.penetration/012-iam.png)

2. Thực hiện xóa
  + Click **Actions** > **Delete**.
  + Bỏ chọn **Create final snapshot** và **Retain automated backups**.
  + Chọn **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**
  + Điền vào ô trống **delete me**.
  + Click **Delete**.

![S3](/images/4.penetration/013-iam.png)
![S3](/images/4.penetration/014-iam.png)

3. Thông báo xóa thành công

![Clean](/images/5.clean/001-cleanaws.png)

#### Xóa CloudWatch

1. Truy cập [giao diện quản trị dịch vụ CloudWatch](https://console.aws.amazon.com/cloudwatch/)
  + Click **Dashboard**.
  
![S3](/images/4.penetration/019-iam.png)

2. Click **RDS-Security-Metrics**.
  
![S3](/images/4.penetration/020-iam.png)

3. Thực hiện xóa CloudWatch
  + Click **Actions** > **Delete dashboard**.
  + Sau khi hiện thông báo, nhấn **Delete**.

![S3](/images/4.penetration/021-iam.png)

3. Xóa thành công

![Clean](/images/5.clean/002-cleanaws.png)

#### Xóa Parameter group

1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Click **Parameter group**.
  
![Clean](/images/5.clean/003-cleanaws.png)

2. Click chọn **custom-mysql8-log**
  + Click **Actions**.
  + Click **Delete**.
  
![Clean](/images/5.clean/004-cleanaws.png)

3. Thực hiện xóa thành công

![Clean](/images/5.clean/005-cleanaws.png)

