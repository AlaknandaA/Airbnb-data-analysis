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
1. room_type (Entire home/apt, Private room, Shared room)
2. neighbourhood_group (many per neighbourhood)
3. neighbourhood (Bronx, Brooklyn, Manhattan, Queens, Staten Island)

Continuous Variables:
1. Price
2. minimum_nights
3. number_of_reviews
4. reviews_per_month
5. calculated_host_listings_count
6. availability_365

Location variables:
1. latitude
2. longitude

Time variable:
1. last_review

## Analysis Methodology

### Data Cleaning

1. Checked datatypes and nulls in each column. The only two column that have significant number of nulls(~20%) are last_review and reviews_per_month. I let those nulls remain.
2. price variable mean is much higher that median, which means that distribution is right skewed. I have kept this as is though, and not applied any transformation to make it more normal, as it was not affecting my analysis and insights significantly.

### Analysis and Visualization

## 1. Analysis of no. of rooms for rent by minimum_nights

![Alt text](images/Number_of_rooms_for_rent_vs_minimum_nights.png?raw=true"Title")

Most people prefer to rent airbnb rooms for one-three night, though there are spikes at 7, 10 and 14 days too.


## 2. Analysis of neighbourhood_group by minimum_nights

![Alt text](images/Different_Neighbourhoods'_number_of_rooms_for_rent_at_different_minimum_nights.png?raw=true"Title")

Manhattan and Brooklyn are the neighbourhoods getting a lot of people renting rooms for 30 days.\
Staten Island and Bronx is not a very popular spot to rent rooms.

## 3. Price and no. of rooms variation per neighbourhood - Bronx

![Alt text](images/Room_prices_and_number_of_rooms_for_rent_in_each_neighbourhood_of_Bronx.png?raw=true"Title")

In above map, colour is adjusted according to the sum of prices of rooms in the particular neighbourhood. Size according to the number of rooms for rent rooms in that neighbourhood.\
In the neighbourhood of Bronx, following are the hottest spots for rooms:

>Kingsbridge(Price=5455, no of rooms=70)\
>Longwood(Price=5699, no of rooms=62)\
>Fordham(Price=4375, no of rooms=63)\
>Mott Haven(Price=5335, no of rooms=60)\
>Concourse(Price=4309, no of rooms=50) are the hottest spots for rooms.

## 4. Price and no. of rooms variation per neighbourhood - Brooklyn

![Alt text](images/Room_prices_and_number_of_rooms_for_rent_in_each_neighbourhood_of_Brooklyn.png?raw=true"Title")

In above map, colour is adjusted according to the sum of prices of rooms in the particular neighbourhood. Size according to the number of rooms for rent rooms in that neighbourhood.\
In the neighbourhood of Brooklyn, following are the hottest spots for rooms:

>Williamsburg (Price=563707, no of rooms=3920)\
>Bedford-Stuyvesant (Price=399917, no of rooms=3714)\
>Bushwick (Price=209033, no of rooms=2465) are the hottest spots for rooms.

## 5. Price and no. of rooms variation per neighbourhood - Manhattan

![Alt text](images/Room_prices_and_number_of_rooms_for_rent_in_each_neighbourhood_of_Manhattan.png?raw=true"Title")

In above map, colour is adjusted according to the sum of prices of rooms in the particular neighbourhood. Size according to the number of rooms for rent rooms in that neighbourhood.\
In the neighbourhood of Manhattan, following are the hottest spots for rooms:

>Harlem (Price=316233, no of rooms=2658)\
>Hell's Kitchen (Price=400987, no of rooms=1958)\
>Upper West Side (Price=415720, no of rooms=1971)\
>East Village (Price=344812, no of rooms=1853)\
>Upper East Side (Price=339729, no of rooms=1800) are the hottest spots for rooms.

## 6. Price and no. of rooms variation per neighbourhood - Queens
 
![Alt text](images/Room_prices_and_number_of_rooms_for_rent_in_each_neighbourhood_of_Queens.png?raw=true"Title")

In above map, colour is adjusted according to the sum of prices of rooms in the particular neighbourhood. Size according to the number of rooms for rent rooms in that neighbourhood.\
In the neighbourhood of Queens, following are the hottest spots for rooms:

>Astoria (Price=105469, no of rooms=900)\
>Long Island City (Price=68449, no of rooms=537) are the hottest spots for rooms.


## 7. Price and no. of rooms variation per neighbourhood - Staten Island

![Alt text](images/Room_prices_and_number_of_rooms_for_rent_in_each_neighbourhood_of_Staten_Island.png?raw=true"Title")

In above map, colour is adjusted according to the sum of prices of rooms in the particular neighbourhood. Size according to the number of rooms for rent rooms in that neighbourhood.\
In the neighbourhood of Staten Island, following are the hottest spots for rooms:

>Randall Manor (Price=6384, no of rooms=19)\
>St. george (Price=5671, no of rooms=48)\
>Tompkinsville (Price=3200, no of rooms=42) are the hottest spots for rooms.


**Useful insights gained from above analysis**:\
* Brooklyn is the best neighbourhood_group to have more number of rooms, since the prices are very high and it also seems very popular.

**Advice for Airbnb Executives**:\
* To increase density of airbnb's around WIlliamsburg, Bedford-Stuyvesant and Bushwick as they are all located closeby.
* Manhattan is also a very popular neighbouhood_group. Can increase density of rooms in north Manhattan vicinity of Harlem and Upper East Side.


## 8. Analysing mean price per neighbourhood in each neighbourhood_group for all neighbourhood_groups

![Alt text](images/Mean_Price_per_neighborhood.png?raw=true"Title")

**Surprising insights**:\
* Two neighbourhoods in Staten Island command very high prices- Fort Wadsworth and Woodrow, even though Staten Island does not have many airbnb's. These two neighbourhoods also do not have any reviews on airbnb's, so insight is to decrease prices or remove them from airbnb.
* Silver Lake neighbourhood in Staten Island neighbourhood_group is very popular(has many reviews) but price is low. Insight is to increase prices here.
* Two neighburhoods in Queens also command high prices- Belle Harbor and Breezy Point.
* Almost all of Manhtaan commands high prices as expected.
* Brooklyn, inspite of having high densities of airbnb's, does not command high prices except in some northern neighbourhoods like Vinegar Hill and Navy Yard, and even that could be due to their proximity to Manhattan.

**Advice for Airbnb Executives**:\
Decrease no of airbnb's in neighbourhoods of Brooklyn which don't command high prices. It may be due to oversaturation.

## 9. Analysing price with limit on number_of_reviews

![Alt text](images/Mean_Price_per_neighbourhood_with_no_of_reviews_less_than_5.png?raw=true"Title")

1. Neighbourhood New Drop in Staten Island does not seem to be very popular as it has 0 reviews and price is also low which means that the airbnb must not be very good. So drop all properties from this neighbourhood from airbnb.
2. Fort Wadsworth and Woodrow from Staten Island, Sea Gate from Brooklyn and Breezy Point from Queens should be dropped from airbnb as they have very high prices but no visitors.

## 10. Analysing number_of_reviews vs availability_365

![Alt text](images/Availability365_vs_no_of_reviews.png?raw=true"Title")

We can see clear dips in the graph in two spots-\
1. At around minimum_nights = 90
2. At around minimum_nights = 180

**Insight**:\
Discourage airbnb owners to keep airbnb's available for 88-90 days and 176-181 days ans people prefer renting for either 3months or 6months, and these figures are just 2-3 days less than 3months/6months.

## 11. Breakup of room type by percentage

![Alt text](images/RoomType_breakup.png?raw=true"Title")

Entire home/apt and private room are for rent in almost equal numbers. Shared rooms are very less as people prefer privacy.

## 12. Room_type vs neighbourhood_group

![Alt text](images/No_of_rooms_per_room_type_per_neighbourhood_group.png?raw=true"Title")

1. Brooklyn and Manhattan are the most popular neighbourhood groups for rooms. In Brooklyn the most popular room type is Private room(50.4%) by a small margin over Entire home/apt(47.5%), and in Manhattan it is Entire home/apt(61%) by a huge margin over private room(37%).
2. Shared rooms are not very popular among travellers. The maximum % they constitute in any region of the total no of rooms for rent is 5% in Bronx.

## 13. Plotting all room_types per neighbourhood on map- Brooklyn

![Alt text](images/Spread_of_different_types_of_rooms_in_Brooklyn.png?raw=true"Title")

Can see almost equal number of blues and reds.\
1. Very dense packing of both private room and Entire home/apt in area of Williamsburg, Bedford-Stuyvesant.
2. Dense packing of Private room in Bushwick.
3. Moderate packing of private room and Entire home/apt in area of Greenpoint.

## 14. Plotting all room_types per neighbourhood on map- Bronx

![Alt text](images/Spread_of_different_types_of_rooms_in_Bronx.png?raw=true"Title")

Can clearly see more blues(more private rooms) than reds(Entire home/apt) in Bronx. Almost 60% airbnb's in Bronx are private rooms, and around 39% entire home/apt.\
1. All airbnb's are quite spread out in general, but can see some clustering at Concourse and Mott Haven.


## 15. Plotting all room_types per neighbourhood on map- Manhattan

![Alt text](images/Spread_of_different_types_of_rooms_in_Manhattan.png?raw=true"Title")

Very high presence of both Entire home/apt and Private room in Manhattan.\
1. Clustering of Private rooms in north Harlem and Entire home/apt in south Harlem.
2. Clustering of Private rooms in north part of Upper West Side and Upper East Side neighbourhoods, and surprisingly little presence of in rest of this neighbourhood. The rest of these neighbourhoods thick clusters of Entire home/apt.
3. Clustering of shared room in Hell's Kitchen neighbourhood, and some presence of Shared rooms in Kips Bay. Very little to none shared rooms in rest of Manhattan.
4. Very thick clustering of Entire home/apt in neighbourhoods of Chelsea, Kips Bay and West Village.
5. Very thick clustering of both Entire home/apt and Private rooms in neighbourhood of East Village and Lower East Side.
6. Small cluster of Entire home/apt in Financial District.

## 16. Plotting all room_types per neighbourhood on map- Queens

![Alt text](images/Spread_of_different_types_of_rooms_in_Queens.png?raw=true"Title")

Sparse distribution of airbnb's throughout Queens except the NorthWestern part.\
1. Thick clustering of Private rooms in Astoria, smaller cluster of Entire home/apt in Astoria too.
2. Small clusters of Private room in Sunny Side, and Ridgewood.

## 17. Plotting all room_types per neighbourhood on map- Staten Island

![Alt text](images/Spread_of_different_types_of_rooms_in_StatenIsland.png?raw=true"Title")

Very sparse distribution on airbnb's.\
1. No clusters per say except small cluster of private room in St. George.

## 18. Price by room type

![Alt text](images/Price_dist_by_room_type.png?raw=true"Title")

Median price of Entire home/apt is higher than Private room and shared room. Insight to airbnb is: Increase the listings of entire home/apt.\
1. Clearly see that price for entire home/apt is slightly higher than private room, we would have expected there to be a much larger gap between the price of the two.
2. There are more private rooms to rent on the lower price side of private rooms, whereas more entire home/apt for rent on the higher side of price for entire home/apt.
3. Shared room is much cheaper than both private room and entire home/apt, but is very low in demand and hence very low in supply.

## 19. Price vs. no. of rooms for each room type

![Alt text](images/Price_vs_no_of_rooms.png?raw=true"Title")

1. Private room on average costs lesser than entire home/apt.
2. Entire home/apt are spread over a large price range- some are cheaper than private rooms and others are expensive.
3. Shared rooms as expected have the least pricing.

## 20. Number of reviews by neighbourhood

![Alt text](images/Neighbourhood_by_no_of_reviews.png?raw=true"Title")

**Insights**:
1. Bedford-Stuyvesant in Brooklyn has the highest number of reviews- seems to be popular.
2. Harlem in Manhattan and Williamsburg in Brooklyn also seem to be quite popular- they too have many reviews.
