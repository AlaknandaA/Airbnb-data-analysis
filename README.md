# Airbnb-data-analysis
To increase Airbnb revenue in 5 neighbourhoods after Corona slowdown, using python and plotly

## Problem Statement

For the past few months, Airbnb has seen a major decline in revenue. Now that the restrictions have started lifting and people have started to travel more, Airbnb wants to make sure that it is fully prepared for this change.

The different leaders at Airbnb want to understand some important insights based on various attributes in the dataset so as to increase the revenue such as -

Which type of hosts to acquire more and where?\
The categorisation of customers based on their preferences.\
What are the neighbourhoods they need to target?\
What is the pricing ranges preferred by customers?\
The various kinds of properties that exist w.r.t. customer preferences.\
Adjustments in the existing properties to make it more customer-oriented.\
What are the most popular localities and properties in New York currently?\
How to get unpopular properties more traction? and so on...

As a data analyst working at Airbnb, I have been assigned the task of extracting insights and presenting them to the management.

**Short Description of data**

The data is for 5 neighbourhoods of New York- Manhattan, Brooklyn, Queens, Bronx and Staten Island.

Column | Column Description
--- | --- 
id | listing id
name | name of listing
host_id | host ID
host_name | name of the host
neighbourhood_group | location
neighbourhood | area 
latitude | latitude coordinates
longitude | longitude coordinates
room_type | listing space type
price | price of room
minimum_nights | amount of minimum nights room can be rented for
number_of_reviews | number of reviews
last_review | latest review
reviews_per_month | number of reviews per month
calculated_host_listings_count | amount of listing per host
availability_365 | number of days of a year that listing is available for booking

Categorical variables:
1. room_type (Entire home/apt, Private room, Shared room)\
2. neighbourhood_group (many per neighbourhood)\
3. neighbourhood (Bronx, Brooklyn, Manhattan, Queens, Staten Island)

Continuous Variables:
1.Price\
2.minimum_nights\
3.number_of_reviews\
4.reviews_per_month\
5.calculated_host_listings_count\
6.availability_365

Location variables:
1. latitude\
2. longitude

Time variable:
1. last_review

## Analysis Methodology

### Data Cleaning

1. Checked datatypes and nulls in each column. The only two column that have significant number of nulls(~20%) are last_review and reviews_per_month. I let those nulls remain.
2. price variable mean is much higher that median, which means that distribution is right skewed. I have kept this as is though, and not applied any transformation to make it more normal, as it was not affecting my analysis and insights significantly.

### Analysis and Visualization

1. ![Alt text](images/Number_of_rooms_for_rent_vs_minimum_nights.png?raw=true"Title")

Most people prefer to rent airbnb rooms for one-three night, though there are spikes at 7, 10 and 14 days too.


2. ![Alt text](images/Different_Neighbourhoods'_number_of_rooms_for_rent_at_different_minimum_nights.png?raw=true"Title")

Manhattan and Brooklyn are the neighbourhoods getting a lot of people renting rooms for 30 days.\
Staten Island and Bronx is not a very popular spot to rent rooms.

3. ![Alt text](images/Different_Neighbourhoods'_number_of_rooms_for_rent_at_different_minimum_nights.png?raw=true"Title")
