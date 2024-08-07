# "Revenue by Film, Genre & Country"

``` SQL SELECT DISTINCT total_revenue.film_id, film.title,SUM(total_revenue.amount) AS total_revenue_per_film, total_revenue.name AS name_of_genre
FROM film
JOIN
(SELECT A.payment_id, A.rental_id, A.amount, D.film_id, D.title, SUM(A.amount) AS total_revenue_per_film, F.name
FROM payment A
INNER JOIN rental B ON A.rental_id = B.rental_id
INNER JOIN inventory C ON B.inventory_id = C.inventory_id
INNER JOIN film D ON C.film_id = D.film_id
INNER JOIN film_category E on D.film_id = E.film_id
INNER JOIN category F on E.category_id = F.category_id
GROUP BY A.payment_id, A.rental_id, A.amount, D.film_id, D.title, F.name
ORDER BY ""total_revenue_per_film"" DESC) AS total_revenue -- subquery renamed total_revenue 
ON total_revenue.film_ID = film.film_ID
GROUP BY total_revenue.film_id, film.title, total_revenue.name
ORDER BY total_revenue_per_film DESC
```