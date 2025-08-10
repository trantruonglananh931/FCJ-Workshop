---
title : "Tạo bảng trong database"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 3.2.1 </b> "
---
#### Tạo bảng trong database.

1. Để tạo được bảng ta sẽ vào database đã được tạo ở lúc cấu hình RDS.
 + Sử dụng lệnh **USE your_database_name;**, với tên database bạn đã cấu hình lúc tạo RDS.

![Connect](/images/3.connect/003-createtable.png)

2. Tạo 1 bảng **users** đơn giản để sử dụng.
  + CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
  + Dùng lệnh **SHOW TABLES;** để xem đã được tạo thành công hay chưa.

![Connect](/images/3.connect/004-createtable.png)

3. Thêm dữ liệu vào bảng **users**.
  + INSERT INTO users (username, email) VALUES 
    ('alice', 'alice@example.com'),
    ('bob', 'bob@example.com');
  + Dữ liệu dc mã hoá at rest vì đã enable encryption.
  + Dùng lệnh **SELECT * FROM users;** để kiểm tra.

![Connect](/images/3.connect/005-createtable.png)
