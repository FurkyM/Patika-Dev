# Homework-9

## City tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```
SELECT city,country 
FROM city
INNER JOIN country ON
city.city_id=country.country_id
;
```
## Customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```
SELECT payment_id, first_name, last_name 
FROM customer
INNER JOIN payment 
ON customer.customer_id=payment.customer_id;
```
## Customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```
SELECT rental_id, first_name, last_name 
FROM customer
INNER JOIN rental
ON customer.customer_id=rental.customer_id;
```
