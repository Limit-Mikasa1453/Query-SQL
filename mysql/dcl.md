# definisi
Data Control Language `DCL` adalah perintah SQL untuk kontrol dan permission database

Terutama untuk hal yang penting. DCL terbagi dalam dua perintah utama yakni:

GRANT  -> Memberikan hak akses / hak istemewa pengguna
```ruby
ex : GRANT SELECT,INSERT, UPDATE, DELETE ON *.* TO 'ngodingdata'@'localhost';
```
REVOKE -> Menarik hak akses pengguna yang diberikan lewat perintah GRANT
```ruby
ex : REVOKE ALL ON nama_database.nama_table FROM 'username'@'localhost';
```
