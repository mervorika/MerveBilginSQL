# ÖDEV 4 - DVD Rental Veritabanı Sorguları

## 1. Film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

```sql
SELECT DISTINCT replacement_cost FROM film;
```
![Alt text](/odev4soru1.png?raw=true "Optional Title")
## 2. Film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
```sql
SELECT COUNT(DISTINCT replacement_cost) FROM film;
```
![Alt text](/odev4soru2.png?raw=true "Optional Title")
## 3. Film tablosunda bulunan film isimlerinde (title) kaç tanesi 'T' karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

```sql
SELECT COUNT(*) FROM film WHERE title LIKE 'T%' AND rating = 'G';
```
![Alt text](/odev4soru3.png?raw=true "Optional Title")
## 4. Country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?

```sql
SELECT COUNT(*) FROM country WHERE LENGTH(country) = 5;
```
![Alt text](/odev4soru4.png?raw=true "Optional Title")
## 5. City tablosundaki şehir isimlerinin kaç tanesi 'R' veya 'r' karakteri ile biter?

```sql
SELECT COUNT(*) FROM city WHERE city ILIKE '%r';
```
![Alt text](/odev4soru5.png?raw=true "Optional Title")