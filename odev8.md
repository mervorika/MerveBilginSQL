# ÖDEV 8 - DVD Rental Veritabanı Sorguları

## Test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee (
	id INTEGER PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
);
```
![Alt text](/odev8soru1.png?raw=true "Optional Title")
## Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
INSERT INTO employee (name, birthday, email) VALUES
('John Doe', '1990-01-15', 'john.doe@example.com'),
('Jane Smith', '1985-05-20', 'jane.smith@example.com'),
-- Diğer 47 adet veri
('Alice Johnson', '1988-09-10', 'alice.johnson@example.com');

```
![Alt text](/odev8soru2.png?raw=true "Optional Title")
## Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```
UPDATE employee SET email = 'Fredek.Pankethman.updated@example.com' WHERE name = 'Fredek Pankethman';
UPDATE employee SET birthday = '1985-05-21' WHERE name = 'Trevar McVeagh';
UPDATE employee SET name = 'Alice Brown' WHERE email = 'kafonsoe@mail.ru';
UPDATE employee SET name = 'New Employee', email = 'new.employee@example.com' WHERE id = 3;
UPDATE employee SET email = 'updated.email@example.com' WHERE birthday BETWEEN '1990-01-01' AND '1993-12-31';

```
![Alt text](/odev8soru3.png?raw=true "Optional Title")
## Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```
DELETE FROM employee WHERE name = 'Fredek Pankethman';
DELETE FROM employee WHERE birthday = '1985-05-21';
DELETE FROM employee WHERE email = 'kafonsoe@mail.ru';
DELETE FROM employee WHERE id = 5;
DELETE FROM employee WHERE birthday BETWEEN '1980-01-01' AND '1992-12-31';
```
![Alt text](/odev8soru4.png?raw=true "Optional Title")