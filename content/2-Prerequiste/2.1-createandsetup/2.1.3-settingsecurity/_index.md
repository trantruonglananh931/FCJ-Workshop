---
title : "Change Securtity group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.1.3 </b> "
---

#### Change Securtity group

In this step, we will modify the Security Group to allow connections from your personal machine.


1. Go to [RDS service management console](https://console.aws.amazon.com/rds/)
  + Click **Database**.
  + Select the database you created.

![VPC](/images/2.prerequisite/001-createdatabase.png)

2. Scroll down **Security group rules**.
  + Click **default (sg-0c641337c0b362188).**

![VPC](/images/2.prerequisite/016-security.png)

3. At **EC2 Console**.
  + Click **sg-0c641337c0b362188**.

![VPC](/images/2.prerequisite/018-security.png)

4. Click **Edit inbound rules**.

![VPC](/images/2.prerequisite/019-security.png)

5. Click **Delete**, then click **Add rule**
  + Change Type to **MySQL/Aurora** and Source to **MyIP**.
  + Click **Save rules**.

![VPC](/images/2.prerequisite/020-security.png)
