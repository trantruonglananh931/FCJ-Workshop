---
title : "Create CloudWatch"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Create Dashboard in CloudWatch

1. Click **Dashboard.**

![VPC](/images/2.prerequisite/011-createcloud.png)

2. Click **Create dashboard.**

![VPC](/images/2.prerequisite/012-createcloud.png)

3. Enter a name of your choice, then click **Create dashboard.**

![VPC](/images/2.prerequisite/013-createcloud.png)

4. Choose **Line**.
  + Click **Next**.

![VPC](/images/2.prerequisite/014-createcloud.png)

5. At form **Add metric graph.**
  + Click **RDS**.
  + Click **DBInstanceIdentifier.**
  + Find and select the following metrics. : **DatabaseConnections**, **FreeStorageSpace**, **ReadIOPS**, **WriteIOPS.**
  + Click **Create widget.**

![VPC](/images/2.prerequisite/015-createcloud.png)
