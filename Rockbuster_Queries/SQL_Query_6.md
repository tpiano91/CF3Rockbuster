# Average Amount Customers Paid to Rent Each Film

```sql
SELECT 
    D.title, 
    AVG(A.amount), 
    F.name AS category_name
FROM 
    payment A
INNER JOIN rental B ON A.rental_id = B.rental_id
INNER JOIN inventory C ON B.inventory_id = C.inventory_id
INNER JOIN film D ON C.film_id = D.film_id
INNER JOIN film_category E ON D.film_id = E.film_id
INNER JOIN category F ON E.category_id = F.category_id
GROUP BY 
    D.title, category_name
ORDER BY 
    AVG(A.amount) DESC
