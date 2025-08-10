---
title : "Quyền của IAM user với RDS"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

1. Truy cập [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iam/)
  + Click **Users**.

![S3](/images/4.penetration/009-iam.png)

2. Tại trang **Users**.
  + Click **rds-auditor**.

![S3](/images/4.penetration/010-iam.png)

3. Tại trang **rds-auditor**
  + Tại dòng **ARN**, sao chép phần số.
  
![S3](/images/4.penetration/011-iam.png)

4. Đăng xuất và đăng nhập lại với IAM

![S3](/images/4.penetration/008-iam.png)

5. Truy cập vào **Aurora and RDS>Databases>securedb**

![S3](/images/4.penetration/012-iam.png)

6. Thực hiện xóa RDS
  + Click **Actions** > **Delete**.
  + Bỏ chọn **Create final snapshot** và **Retain automated backups**.
  + Chọn **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**
  + Điền vào ô trống **delete me**.
  + Click **Delete**.

![S3](/images/4.penetration/013-iam.png)
![S3](/images/4.penetration/014-iam.png)

6. Không thể xóa RDS
  + Không thể xóa vì không đủ quyền, auditor chỉ có quyền đọc.

![S3](/images/4.penetration/015-iam.png)

7. Click **Modify**
  + Đổi tên của RDS

![S3](/images/4.penetration/016-iam.png)

8. Ở mục **Summary of modifications**
  + Chọn **Apply immediately**.
  + Click **Modify DB instance**.

![S3](/images/4.penetration/017-iam.png)

9. Không thành công vì IAM user không có quyền

![S3](/images/4.penetration/018-iam.png)