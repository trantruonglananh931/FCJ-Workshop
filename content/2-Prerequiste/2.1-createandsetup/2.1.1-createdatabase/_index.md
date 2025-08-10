---
title : "Create RDS"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1.1 </b> "
---


#### Create Database **Lab Database**
1. Go to [RDS service management console](https://console.aws.amazon.com/rds/)
  + Click **Create Database**.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. At **Create Database**.
  + In **Choose a database creation method** section, choose **Standard create**.
  + In **Engine options** section, choose **MySQL**.
  + Uncheck **Show only versions that support the Multi-AZ DB cluster** and **Show only versions that support the Amazon RDS Optimized Writes**.
  + **Engine version** use the latest version and uncheck **Enable RDS Extended Support**.
  +  In **Template** section, choose **Free Tier**.

![VPC](/images/2.prerequisite/002-createdatabase.png)
![VPC](/images/2.prerequisite/003-createdatabase.png)

3. At **Setting**.
  + In **DB instance identifier** field, enter **database name**(or a username of your choice).
  + In **Master username** field, enter **admin**.
  + In **Credentials management** section, choose **Self managed**.
  + In **Master password** field, enter **password**.
  + In **Confirm master password** field, re-enter the **password entered above**.

![VPC](/images/2.prerequisite/004-createdatabase.png)

4. At **Instance configuration**.
  + Choose **db.t3.micro**.
  + Leave the remaining settings as default.

![VPC](/images/2.prerequisite/005-createdatabase.png)

5. At **Storage**.
  + Click in **Additional storage configuration**.
  + Uncheck **Enable storage autoscaling**.

![VPC](/images/2.prerequisite/006-createdatabase.png)

5. At **Connectivity**.
  + In **Public access**, choose **Yes**.
  + Leave the remaining settings as default.

![VPC](/images/2.prerequisite/007-createdatabase.png)

6. At **Database authentication**.
  + Choose **Password and IAM database authentication**.

![VPC](/images/2.prerequisite/008-createdatabase.png)

7. At **Monitoring**.
  + In **Log exports**, choose **Audit log**, **Slow query log** and **iam-db-auth-error log**.

![VPC](/images/2.prerequisite/009-createdatabase.png)

8. At **Additional configuration**.
  + In **Initial database name** field, enter **name of database**(or a name of your choice).

![VPC](/images/2.prerequisite/010-createdatabase.png)

9. Scroll to the bottom of the page, click **Create database**.