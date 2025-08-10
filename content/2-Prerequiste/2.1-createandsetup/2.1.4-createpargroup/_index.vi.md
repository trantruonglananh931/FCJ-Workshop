---
title : "Tạo parameter group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.1.4 </b> "
---

#### Tạo parameter group

Trong bước này chúng ta sẽ tiến hành tạo parameter group để có thể gửi log tới CloudWatch.

1. Truy cập [giao diện quản trị dịch vụ RDS](https://console.aws.amazon.com/rds/)
  + Click **Parameter groups**. 
  + Click **Create parameter group**.

![SG](/images/2.prerequisite/021-createpargroup.png)

2. Tại trang **Parameter group details**. 
  + Tại mục **Parameter group name**, điền **custom-mysql8-log**.
  + Tại mục **Description**, điền **Enable general log and export**.
  + Tại mục **Engine type**, chọn **MySQL Community**.
  + Tại mục **Parameter group family**, chọn **mysql8.0**.
  + Tại mục **Type**, chọn **DB Parameter Group**.
  + Click **Create**.

![SG](/images/2.prerequisite/022-createpargroup.png)

3. Nhấn vào **custom-mysql8-log**.

![SG](/images/2.prerequisite/023-createpargroup.png)

4. Click **Edit**.

![SG](/images/2.prerequisite/024-createpargroup.png)

5. Tại thanh tìm kiếm.
  + Tìm **general_log** và chỉnh **value** thành 1.
  + Tìm **log_error_verbosity** và chỉnh **value** thành 3.

![SG](/images/2.prerequisite/025-createpargroup.png)

6. Truy cập vào database của bạn
  + Click vào **Modify**.

![SG](/images/2.prerequisite/026-createpargroup.png)

7. Kéo xuống phần **Additional configuration**
  + Tại phần **DB parameter group** chọn **custom-mysql8-log**.
  + Click **Continue**.

![SG](/images/2.prerequisite/027-createpargroup.png)

8. Mục **Schedule modifications**
  + Click **Apply immediately**.
  + Click **Modify DB instance**.

![SG](/images/2.prerequisite/028-createpargroup.png)

9. Vào lại trang database
  + Click **Action**.
  + Click **Reboot**.
  + Click **Confirm**.

![SG](/images/2.prerequisite/029-createpargroup.png)
