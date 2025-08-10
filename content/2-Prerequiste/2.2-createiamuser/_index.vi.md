---
title : "Tạo IAM User"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo IAM User


1. Truy cập vào [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/)
2. Ở thanh điều hướng bên trái, click  **Users**.  

![role](/images/2.prerequisite/038-iamuser.png)

3. Click **Create user**.  

![role1](/images/2.prerequisite/039-iamuser.png)

4. Tại trang **User details**. 
  + Tại mục **User name** điền **tên user**.
  + Click chọn **Provide user access to the AWS Management Console - optional**.
  + Tại mục **Are you providing console access to a person?** chọn **I want to create an IAM user**.
  + Tại mục **Console password** chọn **Custom password**.
  + Điền mật khẩu vào ô trống, có thể chọn **Show password** để xem mật khẩu.
  + Click bỏ chọn **Users must create a new password at next sign-in - Recommended**.
  + Click **Next**.

![role1](/images/2.prerequisite/040-iamuser.png)

5. Tại trang **Set permissions**. 
  + Tại mục **Permissions options** chọn **Attach policies directly**.
  + Tại mục **Permissions policies**, tìm và chọn **AmazonRDSFullAccess**, **CloudWatchLogsFullAccess** và **AWSKeyManagementServicePowerUser**.
  + Click **Next**.

![createpolicy](/images/2.prerequisite/041-iamuser.png)
![createpolicy](/images/2.prerequisite/042-iamuser.png)
![createpolicy](/images/2.prerequisite/043-iamuser.png)
![createpolicy](/images/2.prerequisite/044-iamuser.png)

6. Tại trang **Review and create**.
  + Kiểm tra lại đầy đủ và chọn **Create user**.

![namerole](/images/2.prerequisite/045-iamuser.png)

6. Tại trang **Retrieve password**.
  + Nhấn **Show** để xem mật khẩu.
  + Có thể tải **User name** và **mật khẩu** về bằng cách bấm vào **Download .csv file**.
  + Click **Return to users list** để hoàn tất.

![namerole](/images/2.prerequisite/046-iamuser.png)

Tiếp theo chúng ta sẽ thực hiện tương tự để tạo thêm 1 IAM User nữa với:
  + Tên user : **rds-auditor.**
  + Permissions policies : **AmazonRDSReadOnlyAccess**, **CloudWatchReadOnlyAccess**.