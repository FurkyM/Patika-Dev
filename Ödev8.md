# Homework-8

## Test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee (
	id INTEGER ,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100));
```
## Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
insert into employee (id, name, birthday, email) values (1, 'Yuri', '2019-06-29', 'ysilkstone0@live.com');
insert into employee (id, name, birthday, email) values (2, 'Bert', '1984-01-05', 'bgott1@guardian.co.uk');
insert into employee (id, name, birthday, email) values (3, 'Dania', '1931-10-04', 'deade2@mysql.com');
...
```
## Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```
UPDATE employee
SET name = 'Mehmet'
WHERE name = 'Yuri';

UPDATE employee
SET email = 'crazyboy_58@patika.com'
WHERE id= 45;

UPDATE employee
SET id = 58
WHERE id = 35;

UPDATE employee
SET birthday = '1999-01-01'
WHERE birthday = '2002-02-02';
```
## Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```
DELETE FROM employee
WHERE id = 9;

DELETE FROM employee
WHERE name = 'Terese';

DELETE FROM employee
WHERE birthday = '1984-01-05';

DELETE FROM employee
WHERE email = 'hmarsdens@reverbnation.com';

DELETE FROM employee
WHERE name = 'Halimeda';
```
