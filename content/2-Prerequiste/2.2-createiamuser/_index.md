---
title : "Create IAM User"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Create IAM User

1. Go to the [IAM service management console](https://console.aws.amazon.com/iamv2/).  
2. In the left navigation pane, click **Users**.  

![role](/images/2.prerequisite/038-iamuser.png)

3. Click **Create user**.  

![role1](/images/2.prerequisite/039-iamuser.png)

4. On the **User details** page:  
   + In **User name**, enter the desired username.  
   + Select **Provide user access to the AWS Management Console - optional**.  
   + For **Are you providing console access to a person?**, choose **I want to create an IAM user**.  
   + For **Console password**, select **Custom password**.  
   + Enter the password in the text box (optionally, select **Show password** to view it).  
   + Uncheck **Users must create a new password at next sign-in - Recommended**.  
   + Click **Next**.

![role1](/images/2.prerequisite/040-iamuser.png)

5. On the **Set permissions** page:  
   + Under **Permissions options**, choose **Attach policies directly**.  
   + In **Permissions policies**, search for and select **AmazonRDSFullAccess**, **CloudWatchLogsFullAccess**, and **AWSKeyManagementServicePowerUser**.  
   + Click **Next**.

![createpolicy](/images/2.prerequisite/041-iamuser.png)  
![createpolicy](/images/2.prerequisite/042-iamuser.png)  
![createpolicy](/images/2.prerequisite/043-iamuser.png)  
![createpolicy](/images/2.prerequisite/044-iamuser.png)

6. On the **Review and create** page:  
   + Review all settings and click **Create user**.

![namerole](/images/2.prerequisite/045-iamuser.png)

7. On the **Retrieve password** page:  
   + Click **Show** to view the password.  
   + You can download the **User name** and **password** by clicking **Download .csv file**.  
   + Click **Return to users list** to complete the process.

![namerole](/images/2.prerequisite/046-iamuser.png)

Next, repeat the same steps to create another IAM User with:  
   + **User name**: **rds-auditor**.  
   + **Permissions policies**: **AmazonRDSReadOnlyAccess**, **CloudWatchReadOnlyAccess**.
