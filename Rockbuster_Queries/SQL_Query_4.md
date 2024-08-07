# "Top Customers by Revenue"

``` SELECT DISTINCT top_customers.customer_id, 
	top_customers.first_name, 
	top_customers.last_name, 
	SUM(top_customers.total_amount_paid),
	top_customers.country,
	top_customers.city
FROM
(SELECT A.customer_id, B.first_name, B.last_name, E.country, D.city, SUM(A.amount)AS total_amount_paid
FROM payment A
INNER JOIN customer B ON A.customer_id = B.customer_id
INNER JOIN address C ON B.address_id = C.address_id
INNER JOIN city D ON C.city_id = D.city_id
INNER JOIN country E ON D.country_ID = E.country_ID
GROUP BY A.customer_id, B.first_name, B.last_name, E.country, D.city 
ORDER BY ""total_amount_paid"" DESC) AS top_customers -- subquery renamed top_customers
GROUP BY top_customers.customer_id, top_customers.first_name, top_customers.last_name, top_customers.total_amount_paid, top_customers.country,top_customers.city
ORDER BY SUM(top_customers.total_amount_paid) DESC
```