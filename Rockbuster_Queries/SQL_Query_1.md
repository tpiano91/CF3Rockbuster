# Rental Duration by Genre & Rental Count

```sql
SELECT name AS name_of_genre, COUNT(A.rental_id) AS total_number_of_rentals, AVG(rental_duration) AS average_rental_duration -- 'name' from film category renamed 'name_of_genre'
FROM rental A
INNER JOIN inventory B ON A.inventory_id = B.inventory_id
INNER JOIN film C ON B.film_id = C.film_id
INNER JOIN film_category D ON C.film_id = D.film_id
INNER JOIN category E ON D.category_id = E.category_id
GROUP BY name
ORDER BY average_rental_duration DESC
