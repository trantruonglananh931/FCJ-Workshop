---
title : "Create parameter group"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.1.4 </b> "
---

#### Create parameter group

In this step, we will create a parameter group to enable sending logs to CloudWatch.

1. Go to [RDS service management console](https://console.aws.amazon.com/rds/)  
   + Click **Parameter groups**.  
   + Click **Create parameter group**.

![SG](/images/2.prerequisite/021-createpargroup.png)

2. At the **Parameter group details** page:  
   + In **Parameter group name**, enter **custom-mysql8-log**.  
   + In **Description**, enter **Enable general log and export**.  
   + In **Engine type**, select **MySQL Community**.  
   + In **Parameter group family**, select **mysql8.0**.  
   + In **Type**, select **DB Parameter Group**.  
   + Click **Create**.

![SG](/images/2.prerequisite/022-createpargroup.png)

3. Click **custom-mysql8-log**.

![SG](/images/2.prerequisite/023-createpargroup.png)

4. Click **Edit**.

![SG](/images/2.prerequisite/024-createpargroup.png)

5. In the search bar:  
   + Search for **general_log** and set its **value** to 1.  
   + Search for **log_error_verbosity** and set its **value** to 3.

![SG](/images/2.prerequisite/025-createpargroup.png)

6. Go to your database:  
   + Click **Modify**.

![SG](/images/2.prerequisite/026-createpargroup.png)

7. Scroll down to **Additional configuration**:  
   + In **DB parameter group**, select **custom-mysql8-log**.  
   + Click **Continue**.

![SG](/images/2.prerequisite/027-createpargroup.png)

8. In the **Schedule modifications** section:  
   + Click **Apply immediately**.  
   + Click **Modify DB instance**.

![SG](/images/2.prerequisite/028-createpargroup.png)

9. Go back to the database page:  
   + Click **Action**.  
   + Click **Reboot**.  
   + Click **Confirm**.

![SG](/images/2.prerequisite/029-createpargroup.png)
