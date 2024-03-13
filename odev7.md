# ÖDEV 7 - DVD Rental Veritabanı Sorguları

## 1. Film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
```sql
SELECT rating, COUNT(*) FROM film
GROUP BY rating;
```
![Alt text](/odev7soru1.png?raw=true "Optional Title")
## 2. Film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50'den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
```sql
SELECT replacement_cost, COUNT(*) as film_sayisi FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY film_sayisi DESC;
```
![Alt text](/odev7soru2.png?raw=true "Optional Title")
## 3. Customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
```sql
SELECT store_id, COUNT(*) as musteri_sayisi FROM customer
GROUP BY store_id;
```
![Alt text](/odev7soru3.png?raw=true "Optional Title")
## 4. City tablosunda bulunan şehir verilerini country_id sütununa göre gruplandıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
```sql
SELECT country_id, COUNT(*) as sehir_sayisi FROM city
GROUP BY country_id
ORDER BY sehir_sayisi DESC
LIMIT 1;
```
![Alt text](/odev7soru4.png?raw=true "Optional Title")