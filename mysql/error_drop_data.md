# Cannot Drop Database
> cara menghapus database yang tidak bisa dihapus melalui frond-end database itu sendiri (phpMyadmin)

## TIDAK BISA DROP DATABASE OR TABLE
permasalahan awal saya `membackup data` melalui sub-directory yang terletak di `/opt/lampp/var/mysql` setelah itu saya hapus directory yang sama dengan nama database. dikemudian hari `lampp` nya saya `uninstall dan install` lagi dikarenakan ga mau ribet `upgrade versi php` hehe maklum masih newbi. nah setelah lampp ketika akses melalui localhost/phpmyadmin dan ada beberapa database lama yang masih terbaca dan ketika mau di drop malah ga bisa muncul pesan error
  
> Error Code: 1558 Column count of mysql.proc is wrong. Expected 21, found 20. Created with MariaDB 100108, now running 100413. 
> Please use mysql_upgrade to fix this error
 
pas dicari di google nemunya [`stackoverflow`](https://stackoverflow.com/questions/16177465/column-count-of-mysql-proc-is-wrong-expected-20-found-16-the-table-is-probabl) dan disarankan untuk `mengupgrade` versi mysql. dan akhirnya saya ikutin saran dari mba.
 
## UPGRADE MYSQL
```ruby
$ mysql_upgrade -u root -p 
```
jika tidak bisa lakukan cara cli dibawah ini. untuk memaksa upgrade versi mysql
```ruby
$ cd /opt/lampp/bin
```
```ruby
$ sudo ./mysql_upgrade OR sudo ./mysql_upgrade --force
```

## HASUS FOLDER DB MYSQL
setelah cara diatas dijalankan database yang tidak bisa dihapus tadi masih tetap ada tapi pesan error ny besa lagi error droping databse 
`can't rmdir './test'. error: 39 "Directory not empty"`
  
cara penyelesaiannya hapus saja folder database mysqll nya yang terletak di /opt/lampp/var/mysql/
  ```ruby
  $ cd /opt/lampp/var/mysql
  ```
  ```ruby
  $ sudo rm -rf <nama_db or nama_diertory_db>
  ```
  
## resources  
* [memperbaiki error drop database di mysql](https://www.primasaja.com/2017/02/Cara-Memperbaiki-Error-no-39-Error-Dropping-Database.html)
  
  selesai deh. semoga membantu. pulpen dan buku adalah senjata yang sering dilupakan

