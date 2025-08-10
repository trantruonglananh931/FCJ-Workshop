---
title : "Phân quyền user với quyền query trong database"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---


Trong bước này, chúng ta sẽ thực hiện query với 2 user với 2 quyền khác nhau.


#### Sử dụng use workshop_db để sử dụng database được phân quyền

1. Kiểm tra quyền select với **auditor**
  + **select * from users;**.

![S3](/images/4.penetration/004-user.png)

2. Kiểm tra các quyền insert, delete, update với **auditor**.
  + **INSERT INTO users (username, email, created_at) VALUES ('charlie', 'charlie@example.com', NOW());**.
  + **DELETE FROM users WHERE id = 2;**.
  + **UPDATE users SET email = 'bob@newmail.com' WHERE username = 'bob';**.

![S3](/images/4.penetration/005-user.png)

**auditor** chỉ có quyền select với database **workshop_db**.

3. Kiểm tra quyền select với **admin1**
  + **select * from users;**.

![S3](/images/4.penetration/006-user.png)

4. Kiểm tra các quyền insert, delete, update với **admin1**.
  + **INSERT INTO users (username, email, created_at) VALUES ('charlie', 'charlie@example.com', NOW());**.
  + **DELETE FROM users WHERE id = 2;**.
  + **UPDATE users SET email = 'bob@newmail.com' WHERE username = 'bob';**.

![S3](/images/4.penetration/007-user.png)

**admin1** có quyền select và insert với database **workshop_db**.