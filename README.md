# NYC-Green-Taxi-Trips-Analysis
A repository for the analysis of the records of Green Taxi Trips in New York City from the year 2017 to 2020. <br />
The datasets used for this project can be accessed using the link: https://drive.google.com/drive/folders/16oUNVhNnB4EN_JQszDK5EmA-vnl28OmT?usp=sharing. <br />

## Introduction
In this project, I analysed the records of Green Taxi Trips in New York City from the year 2017 to 2020. <br />
The aim of this project is;
* Increase the revenue to be generated for the following year. <br />
* Predict the average fare amount per trip to be collected next week. <br />
* Find the days of the week and times of the day that are the busiest. <br />
* Find the most popular pick-up and drop-off locations. <br />

## Data Cleaning
The datasets of this project contains 6 CSV files and a geospatial map in TopoJSON format. The raw data files for the taxi trips needed a lot of cleaning and preparation. I imported the files into Microsoft PowerBI Query Editor and performed the following cleaning processes;
* Filtered out trips that were NOT sent via “store and forward”.
* Filtered only street-hailed trips paid by card or cash with a standard rate
* Filtered out trips with dates before 2017 or after 2020.
* Filtered out pickups and dropoffs zones to unknown locations.
* Replaced any trips having no recorded passengers with 1 passenger.
* Filtered out trips lasting longer than a day.
* For trips whose pickup date/time were after the dropoff date/time, I swapped the pickup date/time and the dropoff date/time.
* For trips where the fare amount, taxes, and surcharges were ALL negative, I replaced them with positive values.
* For trips that have a fare amount but have a trip distance of 0, I calculated the distance as (Fare amount - 2.5) / 2.5.
* For trips that have a trip distance but have a fare amount of 0, I calculated the fare amount as 2.5 + (trip distance x 2.5)

## Data Exploration
After the cleaning and preparation processes, the following are some of the key insights I generated;
* The Total Taxi Trips for the 4-year period = 26 Million trips
* The Total Revenue generated = 387 Million dollars
* The Total Number of Passengers = 35 Million
* The Average Fare collected per trip = $12.28
* The Most Used Payment Type = Credit Card

## Insights From My Analysis
* __Average Fare Amount to expect next week__: The average fare amount to expect next week (Week 21) is $12.96.
* __Total Amount Charged to Passengers By Week of the Year__: 'Week 4' has $9,314,161 as the highest total amount charged while 'Week 47' has $4,916,624 as the least total amount charged.
* __Average Fare Collected By Week of the Year__: 'Week 31' has $12.99 as the highest average fare collected while 'Week 4' has $11.74 as the least average fare collected.
* __Total Trips By Day of the Week__: 'Saturday' records 4,069,766 total trips as the highest while 'Monday' records 3,174,336 total trips as the least.
* __Total Trips By Time of the Day__: '12:00:00 AM' records 774 total trips as the time of the day with the highest number of total trips while '5:20:33 AM' records 37 total trips as the least.
* __Total Trips By Payment Type__: 'Credit Card' has 54.29% with 14,225,937 total trips while 'Cash' has 45.71% with 11,979,856 total trips.
* __Total Trips By VendorID__: 'Verifone Inc.' has 21,695,728 total trips while 'LLC' has 4,510,065 total trips.
* __Total Trips By Borough__: 'Manhattan' has the highest records of 8,887,133 total trips while 'EWR' has the least with 67 total trips.
* __Most Popular Pickup Location__: 'East Harlem North' is the most popular pickup location with 1,833,791 total trips while 'Governor's Island/Ellis Island/Liberty Island' are the least popular pickup locations with 1 total trip.
* __Most Popular Dropoff Location__: 'East Harlem North' is the most popular dropoff location with 956,053 total trips while 'Great Kills Park' is the least popular dropoff location with 1 total trip.

## Recommendations
From my analysis, I recommend that more taxi cabs should be made available to pickup and dropoff passengers;
* In Manhattan
* In the most popular pickup and dropoff locations such as 'East Harlem North', 'East Harlem South', 'Central Harlem North', 'Central Harlem', 'Astoria' etc.
* On Saturdays every weekend by 12:00:00 AM.
* In the '4th Week' of every year.
* From 'Verifone Inc.'.

## Relevant Links
* [Report Presentation](https://www.linkedin.com/posts/rukevweevwrujae_data-analytics-bigdata-activity-6897524091298144256-F5pG?utm_source=linkedin_share&utm_medium=member_desktop_web)
* [LinkedIn](https://www.linkedin.com/in/rukevweevwrujae/)
