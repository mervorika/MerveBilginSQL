# ÖDEV 11 - DVD Rental Veritabanı Sorguları

## Actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım:
```
SELECT first_name FROM actor
UNION
SELECT first_name FROM customer;
```
![Alt text](/odev11soru1.png?raw=true "Optional Title")
## Ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım:
```
SELECT first_name FROM actor
INTERSECT
SELECT first_name FROM customer;
```
![Alt text](/odev11soru2.png?raw=true "Optional Title")
## Actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım:
```
SELECT first_name FROM actor
EXCEPT
SELECT first_name FROM customer;
```
![Alt text](/odev11soru3.png?raw=true "Optional Title")
## İlk 3 sorguyu tekrar eden veriler için de yapalım:

```
SELECT first_name FROM actor
UNION
SELECT first_name FROM customer;


SELECT first_name FROM actor
INTERSECT
SELECT first_name FROM customer;


SELECT first_name FROM actor
EXCEPT
SELECT first_name FROM customer;
```
![Alt text](/odev11soru4.png?raw=true "Optional Title")