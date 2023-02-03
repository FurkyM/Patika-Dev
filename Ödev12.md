# Homework-12

## Film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```
SELECT COUNT(length) from film
WHERE length>(SELECT AVG(length)from film);
```
## Film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
```
SELECT COUNT(*) FROM film
WHERE rental_rate = (SELECT MAX(rental_rate) from film);
```
## Film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
```
SELECT film_id FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) from film) 
AND 
replacement_cost = (SELECT MIN (replacement_cost) from film);
```
## Payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
```
SELECT * FROM customer
WHERE customer_id = ( SELECT customer_id FROM payment GROUP BY customer_id ORDER BY COUNT(customer_id) DESC LIMIT 1);
```
