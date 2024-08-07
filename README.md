# CF3Rockbuster
###### This project was completed as a requirement for the Data Analytics Program by CareerFoundry
## Project Overview
###### "Rockbuster Stealth LLC is a movie rental company that used to have stores around the world. Facing stiff competition from streaming services such as Netflix and Amazon Prime, the Rockbuster Stealth management team is planning to use its existing movie licenses to launch an online video rental service in order to stay competitive.
###### You’ve been hired as a data analyst by Rockbuster Stealth’s business intelligence (BI) department to help with the launch strategy for the new online video service. The BI department helps other departments, from inventory to customer insights, with data-related queries. Your first task is to load all of Rockbuster’s data into a relational database management system (RDBMS). Then, you’ll use SQL to analyze the data and answer any ad-hoc business questions that other departments may have."

##### The SQL queries used for this project can be found in the "Queries" folder

## Key Questions and Objectives
###### Which movies contributed the most/least to revenue gain?
###### What was the average rental duration for all videos?
###### Which countries are Rockbuster customers based in?
###### Where are customers with a high lifetime value based?
###### Do sales figures vary between geographic regions?

## Insights
<div class='tableauPlaceholder' id='viz1723045449486' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ta&#47;Task3_10Updated&#47;TotalRevenuebyMovieGenre&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Task3_10Updated&#47;TotalRevenuebyMovieGenre' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ta&#47;Task3_10Updated&#47;TotalRevenuebyMovieGenre&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1723045449486');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
###### "Sports" genre ranks 1st in both revenue earned and number of films in Rockbuster's inventory.
###### "Sci-Fi" genre ranks 2nd in revenue earned, despite ranking 9th in total number of films in inventory.
###### "Foreign" and "Family" genres rank 2nd and 3rd in total number of films, respectively, but only rank 8th and 10th in total revenue earned.
###### Films across all genres rent for an average of 4.5-5.5 days, with films in the "New" genre having the lowest average of number of days rented
###### Countries with high populations tend to have higher number of Rockbuster customers (the top 3 countries by population are also have the most Rockbuster customers)

## Recommendations
###### Increase the number of "Sci-Fi" and "Sports" films in inventory; decrease the number of "Foreign" and "Family" genres.
###### Conduct further research to determine if "Sci-Fi" films should be rented at a higher price and if "Foreign" and "Family" films should be rented at a lower price.
###### Offer shorter rental periods for "New" films, particularly for films that have recently left theaters; further research can determine the most effective way to market this rental option
###### Emphasize marketing strategies in countries with high populations; further research is needed to see if other factors besides population determine Rockbuster's popularity in a country/region

## Data
##### The dataset contains the following data tables
###### Payment
###### Rental
###### Customer
###### Store
###### film_actor
###### Inventory
###### film_category
###### Staff
###### Actor
###### Film
###### Category
###### Address
###### Language
###### City
###### Country
##### Downloadable link to dataset:
http://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip

## Visualizations
##### Link to Tableau Visualizations (on Tableau Public)
https://public.tableau.com/app/profile/tristan.savella/viz/Task3_10Updated/Top14byCustomerCount

## Tools Used
###### PostgreSQL
###### Tableau
###### Excel
