+++
title = "Clean Up Resources"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

We will perform the following steps to delete the resources created during this lab.  
Use an account with sufficient permissions or the AWS root account.

#### Delete RDS

1. Go to the [RDS management console](https://console.aws.amazon.com/rds/)  
  + Navigate to **Databases > securedb**.

![S3](/images/4.penetration/012-iam.png)

2. Delete the RDS instance:  
  + Click **Actions** > **Delete**.  
  + Uncheck **Create final snapshot** and **Retain automated backups**.  
  + Check **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**  
  + Type **delete me** in the text box.  
  + Click **Delete**.

![S3](/images/4.penetration/013-iam.png)  
![S3](/images/4.penetration/014-iam.png)

3. Confirmation message showing the RDS instance was deleted successfully.

![Clean](/images/5.clean/001-cleanaws.png)

#### Delete CloudWatch Dashboard

1. Go to the [CloudWatch management console](https://console.aws.amazon.com/cloudwatch/)  
  + Click **Dashboard**.

![S3](/images/4.penetration/019-iam.png)

2. Click **RDS-Security-Metrics**.

![S3](/images/4.penetration/020-iam.png)

3. Delete the dashboard:  
  + Click **Actions** > **Delete dashboard**.  
  + When prompted, click **Delete**.

![S3](/images/4.penetration/021-iam.png)

4. Confirmation message showing the dashboard was deleted successfully.

![Clean](/images/5.clean/002-cleanaws.png)

#### Delete Parameter Group

1. Go to the [RDS management console](https://console.aws.amazon.com/rds/)  
  + Click **Parameter group**.

![Clean](/images/5.clean/003-cleanaws.png)

2. Select **custom-mysql8-log**  
  + Click **Actions**.  
  + Click **Delete**.

![Clean](/images/5.clean/004-cleanaws.png)

3. Confirmation message showing the parameter group was deleted successfully.

![Clean](/images/5.clean/005-cleanaws.png)
