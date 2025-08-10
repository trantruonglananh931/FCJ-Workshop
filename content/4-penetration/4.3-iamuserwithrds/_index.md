---
title : "IAM User Permissions with RDS"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

1. Go to the [IAM service management console](https://console.aws.amazon.com/iam/)  
  + Click **Users**.

![S3](/images/4.penetration/009-iam.png)

2. On the **Users** page:  
  + Click **rds-auditor**.

![S3](/images/4.penetration/010-iam.png)

3. On the **rds-auditor** page:  
  + Under **ARN**, copy the numeric portion.

![S3](/images/4.penetration/011-iam.png)

4. Log out and log back in with the IAM account.

![S3](/images/4.penetration/008-iam.png)

5. Navigate to **Aurora and RDS > Databases > securedb**

![S3](/images/4.penetration/012-iam.png)

6. Attempt to delete the RDS instance:  
  + Click **Actions** > **Delete**.  
  + Uncheck **Create final snapshot** and **Retain automated backups**.  
  + Select **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**  
  + Enter **delete me** in the confirmation field.  
  + Click **Delete**.

![S3](/images/4.penetration/013-iam.png)  
![S3](/images/4.penetration/014-iam.png)

6. Unable to delete RDS:  
  + Deletion failed due to insufficient permissions — **auditor** only has read access.

![S3](/images/4.penetration/015-iam.png)

7. Click **Modify**  
  + Attempt to rename the RDS instance.

![S3](/images/4.penetration/016-iam.png)

8. In **Summary of modifications**:  
  + Select **Apply immediately**.  
  + Click **Modify DB instance**.

![S3](/images/4.penetration/017-iam.png)

9. Operation failed — IAM user does not have the necessary permissions.

![S3](/images/4.penetration/018-iam.png)
