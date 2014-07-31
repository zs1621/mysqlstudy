

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
UPDATE  `bcuser` SET  `nick_name` =  '周',
`password` =  '59a46b111fe459b58a170f4f0acdbd945c9fb1db5d71d6f1c38f3765c32a6225',
`email` =  'zsa@11.com',
`phone` =  '13681714904',
`role` = NULL WHERE  `bcuser`.`id` =112 LIMIT 1
```

 - **drop table** 

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



