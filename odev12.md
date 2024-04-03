# ÖDEV 12 - DVD Rental Veritabanı Sorguları

## Film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```
SELECT COUNT(*)
FROM film
WHERE length > (SELECT AVG(length) FROM film);
```
![Alt text](/odev12soru1.png?raw=true "Optional Title")
## Film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
```
SELECT COUNT(*)
FROM film
WHERE rental_rate = (SELECT MAX(rental_rate) FROM film);
```
![Alt text](/odev12soru2.png?raw=true "Optional Title")
## Film tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız.
```
SELECT *
FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film)
AND replacement_cost = (SELECT MIN(replacement_cost) FROM film);
```
![Alt text](/odev12soru3.png?raw=true "Optional Title")
## Payment tablosunda en fazla sayıda alışveriş yapan müşterileri (customer) sıralayınız.
```
SELECT customer_id, COUNT(*) as total_payments
FROM payment
GROUP BY customer_id
ORDER BY total_payments DESC
LIMIT 10; 
```
![Alt text](/odev12soru4.png?raw=true "Optional Title")