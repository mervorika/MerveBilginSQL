# ÖDEV 5 - DVD Rental Veritabanı Sorguları

## 1. film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

```sql
SELECT * FROM film WHERE title LIKE '%n' ORDER BY length DESC LIMIT 5;
```
![Alt text](/odev5soru1.png?raw=true "Optional Title")
## 2. film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
```sql
SELECT * FROM film WHERE title LIKE '%n' ORDER BY length OFFSET 5 LIMIT 5 ;
```
![Alt text](/odev5soru2.png?raw=true "Optional Title")
## 3. customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.

```sql
SELECT * FROM customer WHERE  store_id = 1 ORDER BY last_name DESC LIMIT 4 ;
```
![Alt text](/odev5soru3.png?raw=true "Optional Title")