## limit or fetch
Menampilkan data sebayak data yang kita tentukan menggunakan fungsi `fetch`
```sql
SELECT * FROM struktur_temp
ORDER BY KD_STORE 
OFFSET 5 ROWS
FETCH NEXT 5 ROWS ONLY;
```
