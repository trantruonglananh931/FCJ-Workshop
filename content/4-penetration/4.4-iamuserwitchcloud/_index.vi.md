---
title : "Quyền của IAM user với CloudWatch"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4.4 </b> "
---


1. Truy cập [giao diện quản trị dịch vụ CloudWatch](https://console.aws.amazon.com/cloudwatch/)
  + Click **Dashboard**.
  
![S3](/images/4.penetration/019-iam.png)

2. Click **RDS-Security-Metrics**.
  
![S3](/images/4.penetration/020-iam.png)

3. Thực hiện xóa CloudWatch
  + Click **Actions** > **Delete dashboard**.
  + Sau khi hiện thông báo, nhấn **Delete**.

![S3](/images/4.penetration/021-iam.png)

4. Thực hiện xóa không thành công do không đủ quyền

![S3](/images/4.penetration/022-iam.png)

5. Thực hiện đổi tên CloudWatch
  + Click **Actions** > **Rename dashboard**.

![S3](/images/4.penetration/021-iam.png)

6. Điền tên mới.
  + Sau đó nhấn **Rename dashboard**.

![S3](/images/4.penetration/023-iam.png)

7. Thực hiện đổi tên không thành công do không đủ quyền.

![S3](/images/4.penetration/024-iam.png)
