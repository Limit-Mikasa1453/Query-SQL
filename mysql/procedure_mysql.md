## Create Procedure with query
```sql
DROP PROCEDURE `doWhil`; 
CREATE DEFINER=`root`@`localhost` PROCEDURE `doWhile`() NOT DETERMINISTIC CONTAINS SQL SQL SECURITY DEFINER BEGIN DECLARE i INT DEFAULT 1; 
WHILE (i <= 1000) DO 
  insert into siswa values (null, 'sigit', 123456, 'pasir nangka', null, null); 
  SET i = i+1; 
END WHILE; 
END
```

## Cara Membuat Procedure with front-end / PhpMyadmin
- Localhost/phpmyadmin > Pilih Database > Klik Routines > Add Routines
- Routine name > nama procedure
- Type > bisa procedure/fungtion
- Definition > 
```sql
BEGIN
DECLARE i INT DEFAULT 1; 
WHILE (i <= 1000) DO
    INSERT INTO SISWA VALUES (null, 'sigit', 123456, 'pasir nangka', null, null);
    SET i = i+1;
END WHILE;
END
```
- Is deterministic > unchek
- Adjust privileges > check
- Definer > `root`@`localhost`
