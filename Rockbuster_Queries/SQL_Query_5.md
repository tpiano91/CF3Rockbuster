# "Average Amount Paid per Rental by Country"

``` SQL SELECT DISTINCT A.country, avg(E.amount) AS avg_amt_paid
FROM Country A
INNER JOIN city B ON A.country_id = B.country_id
INNER JOIN address C ON B.city_id = C.city_id
INNER JOIN customer D ON C.address_id = D.address_id
INNER JOIN payment E ON D.customer_id = E.customer_id
INNER JOIN rental F ON E.rental_id = F.rental_id
INNER JOIN inventory G ON F.inventory_id = G.inventory_id
INNER JOIN film H ON G.film_id = H.film_id
INNER JOIN film_category I ON H.film_id = I.film_id
INNER JOIN category J ON I.category_id = J.category_id
GROUP BY A.country
ORDER BY avg_amt_paid DESC
```