

- **create database**

```
CREATE DATABASE database_name;
```


- **delete primary key**


```
ALTER TABLE t_team DROP PRIMARY KEY;  
```
- **modify primary key to auto-increment**


```
ALTER TABLE t_team modify id int AUTO_INCREMENT;
```

- **delete one column**

```
DELETE FROM `table_name` WHERE `table.name`.`id` = 11
```

- **update one column**

```
UPDATE  `table_name` SET  `nick_name` =  '周',
`password` =  '59a46b111fe459b58a170f4f0acdbd945c9fb1db5d71d6f1c38f3765c32a6225',
`email` =  'zs1213yh@gmail.com',
`phone` =  '13681714904',
`role` = NULL WHERE  `bcuser`.`id` =112 LIMIT 1
```

 - **drop table**(这个是直接删除这个表)

```
DROP TABLE `table_name`;
```


 - **show/list users in a mysql database**

```
SELECT * FROM mysql.user;
```

 - **create user in mysql**
 
```
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
```

 - **grant user differe permission**
  - ALL PRIVILEGES - grant all access to a designated database
  - CREATE : allows them to crate new tables or databases
  - DROP : allows them to delete tables or databases
  - DELETE : allows them to delete rows from tables
  - INSERT : allows them to insert rows into tables
  - SELECT : allows them to use the Select command to read through database
  - UPDATE : allow them to update table rows
  - GRANT OPTION : allows them grant or remove other user'privileges


```
GRANT [type of permission] ON [database name].[table name] TO 'username'@'localhost' ;
GRANT ALL PRIVILEGES ON database_name.table_name TO 'username'@'localhost';
```

 - **drop one column from  table**

```
ALTER TABLE  `table_name` DROP  `column_name` ;
```


 - **rename table name**

```
RENAME TABLE  `databasename`.`table_old_name` TO  `databasename`.`table_new_name` ;
```


 - **encode look**

```
SHOW VARIABLES WHERE Variable_name LIKE 'character\_set\_%' OR Variable_name LIKE 'collation%';
```

 - **clean up data from table**

```
TRUNCATE TABLE `table_name`
```

 - **change one column name**

```
ALTER TABLE `table_name` change oldname newname varchar(10)...
```

 - **显示用户**
  - USER() reports how you attempted to authenticate in MySQL
  - CURRENT_USER() reports how you were allowed to authenticate in MySQL

```
SELECT USER(),CURRENT_USER();
```


 - **查看二进制log**
  - 进入log文件目录

```
mysqlbinlog mysql-bin.000001 
```

 - **添加一列(add one column)**

```
alter table table_name add column new_column_name int NOT NULL DEFAULT 0;
```

 - **mysql export to .xls**

```
 mysql your_database  -uroot  -p  -e  "select   *   from   test.table2"   >   /home/test.xls
```

 - **mysql script run in shell**


```
cat filename.sql | mysql -u username -p 
echo "create database databasename" | mysql -u username -p
```



 - **delete foreign key**

```
ALTER TABLE table_name DROP FOREIGN KEY key_name;
SHOW CREATE TABLE table_name;  #这个可以看key_name, 就是 CONSTRAINT 后面的
```

 - **show index**

```
show index from dd_permission;
```

 - **rename table_name**

```
RENAME TABLE old_table_name To new_table_name
```
