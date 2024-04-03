# ÖDEV 10 - DVD Rental Veritabanı Sorguları

## city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusu:
```
SELECT city.city, country.country
FROM city
LEFT JOIN country ON city.country_id = country.country_id;
```
![Alt text](/odev10soru1.png?raw=true "Optional Title")
## customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusu:
```
SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;
```
![Alt text](/odev10soru2.png?raw=true "Optional Title")
## customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusu:
```
SELECT rental.rental_id, customer.first_name, customer.last_name
FROM customer
FULL JOIN rental ON customer.customer_id = rental.customer_id;
```
![Alt text](/odev10soru3.png?raw=true "Optional Title")