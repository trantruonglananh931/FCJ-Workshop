---
title : "User Permissions with Query in the Database"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---

In this step, we will execute queries using two users with different permission levels.

#### Use `use workshop_db` to work with the assigned database

1. Test **SELECT** permission with **auditor**  
  + **select * from users;**

![S3](/images/4.penetration/004-user.png)

2. Test **INSERT**, **DELETE**, and **UPDATE** permissions with **auditor**  
  + **INSERT INTO users (username, email, created_at) VALUES ('charlie', 'charlie@example.com', NOW());**  
  + **DELETE FROM users WHERE id = 2;**  
  + **UPDATE users SET email = 'bob@newmail.com' WHERE username = 'bob';**

![S3](/images/4.penetration/005-user.png)

**auditor** only has **SELECT** permission on the **workshop_db** database.

3. Test **SELECT** permission with **admin1**  
  + **select * from users;**

![S3](/images/4.penetration/006-user.png)

4. Test **INSERT**, **DELETE**, and **UPDATE** permissions with **admin1**  
  + **INSERT INTO users (username, email, created_at) VALUES ('charlie', 'charlie@example.com', NOW());**  
  + **DELETE FROM users WHERE id = 2;**  
  + **UPDATE users SET email = 'bob@newmail.com' WHERE username = 'bob';**

![S3](/images/4.penetration/007-user.png)

**admin1** has both **SELECT** and **INSERT** permissions on the **workshop_db** database.
