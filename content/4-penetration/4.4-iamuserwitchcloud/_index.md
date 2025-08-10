---
title : "IAM User Permissions with CloudWatch"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4.4 </b> "
---

1. Go to the [CloudWatch management console](https://console.aws.amazon.com/cloudwatch/)  
  + Click **Dashboard**.
  
![S3](/images/4.penetration/019-iam.png)

2. Click **RDS-Security-Metrics**.
  
![S3](/images/4.penetration/020-iam.png)

3. Attempt to delete the CloudWatch dashboard:  
  + Click **Actions** > **Delete dashboard**.  
  + When prompted, click **Delete**.

![S3](/images/4.penetration/021-iam.png)

4. Deletion failed due to insufficient permissions.

![S3](/images/4.penetration/022-iam.png)

5. Attempt to rename the CloudWatch dashboard:  
  + Click **Actions** > **Rename dashboard**.

![S3](/images/4.penetration/021-iam.png)

6. Enter a new name.  
  + Then click **Rename dashboard**.

![S3](/images/4.penetration/023-iam.png)

7. Rename action failed due to insufficient permissions.

![S3](/images/4.penetration/024-iam.png)
