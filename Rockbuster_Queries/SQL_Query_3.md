# "Rental Information: Summary Statistics"

``` SELECT MIN(rental_rate) AS min_rent,
       MAX(rental_rate) AS max_rent,
       AVG(rental_rate) AS avg_rent,
	   MIN(release_year)AS min_release_year,
       MAX(release_year) AS max_release_year,
       AVG(release_year) AS avg_release_year,
	   MIN(rental_duration) AS min_rental_duration,
       MAX(rental_duration) AS max_rental_duration,
       AVG(rental_duration) AS avg_rental_duration,
	   MIN(length) AS min_length,
       MAX(length) AS length,
       AVG(length) AS length,
	   MIN(replacement_cost) AS min_replacement_cost,
       MAX(replacement_cost) AS max_replacement_cost,
       AVG(replacement_cost) AS avg_replacement_cost
FROM film
```