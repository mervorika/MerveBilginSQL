# ÖDEV 1 - DVDRental Veritabanı Sorguları

## 1. Film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
```sql
SELECT title, description FROM film;
```
![Alt text](/odev1soru1.png?raw=true "Optional Title")

## 2. Film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
```sql
SELECT * FROM film WHERE length > 60 AND length < 75;
```
![Alt text](/odev1soru2.png?raw=true "Optional Title")
## 3. Film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
```sql
SELECT * FROM film WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```
![Alt text](/odev1soru3.png?raw=true "Optional Title")
## 4. Customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
```sql
SELECT last_name FROM customer WHERE first_name = 'Mary';
```
![Alt text](/odev1soru4.png?raw=true "Optional Title")
## 5. Film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
```sql
SELECT * FROM film WHERE NOT length > 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);
```
![Alt text](/odev1soru5.png?raw=true "Optional Title")