#SQL
## Create User
Use uppercase for commands
`CREATE USER new_username@localhost IDENTIFIED BY 'password';`

creates a local user, and assigns a password

`GRANT ALL PRIVILEGES ON *.* TO new_user@localhost;`

gives `ALL` authority to all (`*.*`) databases to the given user

* Keep permissions minimal
* Make users for different types of access for cleaner logs

##Create A Schema
* A Schema is a database structure

`CREATE SCHEMA zipcode;`

Makes an empty database called `zipcode`

`SHOW DATABASES;`

Shows all databases (see below)
```mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| zipcode            |
+--------------------+
5 rows in set (0.01 sec)
```

## Select Database

## Create Table
```
CREATE TABLE table_name (
  column1 datatype,
  column2 datatype,
  column3 datatype
);
```
`table_name` is the table name of the database being used, or in the format database.tablename

There are extra options to the datatype, common ones
* AUTO_INCREMENT (usefule for unique id, it increases automatically )
* NOT NULL
* PRIMARY KEY

##See a table layout
`DESCRIBE tablename`

## Relationships



INSERT INTO zipcode.teacher_meta (teacher_id, years, room_number)
    VALUES (13, 3, 2),
      (14, 3, 2),
      (15, 10, 1);
