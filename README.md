# :seedling:DASAR Query-SQL
**Query SQL (MySql, Oracle, SqlServer, Postgree, Mongo DB)**

# :shamrock:Data Definition Language (DDL)

Perintah dasar yang pertama yaitu `Data Definition Language` atau biasa disingkat dengan DDL.Perintah ini merupakan perintah yang paling mendasar dari bahasa SQL. Tujuannya untuk membuat struktur sebuah database

- CREATE
```sql
  CREATE DATABASE databasename;
```
```sql
  CREATE Table databasename;
```

- ALTER 
```sql
ALTER TABLE table_name ADD column_name datatype;
```
```sql
  ALTER TABLE table_name DROP COLUMN column_name;
```
MySql/Oracle
```sql
ALTER TABLE table_name MODIFY COLUMN column_name datatype; 
```
MsAcces/SqlServer
```sql
  ALTER TABLE table_name ALTER COLUMN column_name datatype; 
```
Oracle 10g kebawah
```sql
  ALTER TABLE table_name MODIFY column_name datatype;
```

- RENAME
```sql
ALTER TABLE old_table_name RENAME new_table_name;
```
```sql
RENAME TABLE old_table_name TO new_table_name;
```

- DROP dan TRUNCATE
```sql
DROP DATABASE databasename;
```
```sql
DROP TABLE table_name;
```
```sql
TRUNCATE TABLE table_name;
```

# :shamrock:Data Manipulation Language(DML)

DML atau Data Manipulation Language merupakan perintah dasar SQL yang bertujuan untuk memanipulasi data yang ada dalam suatu database

- INSERT
```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```
```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

- SELECT 
```sql
  SELECT column1, column2, ...
  FROM table_name;
```
  
- UPDATE
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
- DELETE
```sql
DELETE FROM table_name WHERE condition;
```

# :shamrock: Transaction Control Language (TCL)
Transaction Control Language (TCL) adalah perintah SQL yang berhubungan dengan transaksi di database Perintah TCL antara lain :

>COMMIT  -> Menyimpan transaksi secara permanen
>ROLLBACK -> Mengembalikan database ke bentuk awal / COMMIT terakhi

- COMMIT
```sql
START TRANSACTION;
INSERT INTO table_name VALUES (value1,value2,value3);
COMMIT;
```
- ROLLBACK
```sql
START TRANSACTION;
INSERT INTO table_name VALUES (value1,value2,value3);
ROOLBACK;
```

#  :shamrock: Data Control Language `DCL`
Data Control Language `DCL` adalah perintah SQL untuk kontrol dan permission database Terutama untuk hal yang penting. DCL terbagi dalam dua perintah utama yakni:

GRANT  -> Memberikan hak akses / hak istemewa pengguna
```sql
ex : GRANT SELECT,INSERT, UPDATE, DELETE ON *.* TO 'ngodingdata'@'localhost';
```
REVOKE -> Menarik hak akses pengguna yang diberikan lewat perintah GRANT
```sql
ex : REVOKE ALL ON nama_database.nama_table FROM 'username'@'localhost';
```

## resource
* [w3sclools](https://www.w3schools.com/sql/)


