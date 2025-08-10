---
title : "Create table in database"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 3.2.1 </b> "
---
#### Create a table in the database.

1. To create a table, first switch to the database that was created during the RDS configuration.
 + Use the command **USE your_database_name;**, replacing `your_database_name` with the database name you set up when creating the RDS instance.

![Connect](/images/3.connect/003-createtable.png)

2. Create a simple **users** table to work with:
  + ```sql
    CREATE TABLE users (
      id INT AUTO_INCREMENT PRIMARY KEY,
      username VARCHAR(50) NOT NULL,
      email VARCHAR(100) NOT NULL UNIQUE,
      created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```
  + Use **SHOW TABLES;** to verify that the table has been successfully created.

![Connect](/images/3.connect/004-createtable.png)

3. Insert data into the **users** table:
  + ```sql
    INSERT INTO users (username, email) VALUES 
      ('alice', 'alice@example.com'),
      ('bob', 'bob@example.com');
    ```
  + The data is encrypted at rest because encryption was enabled.
  + Use **SELECT * FROM users;** to check the inserted data.

![Connect](/images/3.connect/005-createtable.png)
