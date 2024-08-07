# "Number of Customers in Each City"

``` "SELECT C.city, D.country,
       COUNT(customer_id) AS count_of_customers
FROM customer A
INNER JOIN address B ON A.address_id = B.address_id
INNER JOIN city C ON B.city_id = C.city_id
INNER JOIN country D ON C.country_ID = D.country_ID
GROUP BY city,country
ORDER BY count_of_customers DESC"
```