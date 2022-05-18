# NYC-Green-Taxi-Trips-Analysis
A repository for the analysis of the records of Green Taxi Trips in New York City from the year 2017 to 2020. <br />
The datasets used for this project can be found here: https://drive.google.com/drive/folders/16oUNVhNnB4EN_JQszDK5EmA-vnl28OmT?usp=sharing. <br />

## Introduction
In this project, I analysed the records of Green Taxi Trips in New York City from the year 2017 to 2020. <br />
The aim of this project is;
* Predict the average number of trips to expect next week. <br />
* Predict the average fare amount per trip to be collected next week. <br />
* Find the days of the week and times of the day that are the busiest. <br />
* Find the most popular pick-up and drop-off locations. <br />

## Data Exploration
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


After the cleaning and preparation processes, the following are some of the key insights I generated;
* The Total Taxi Trips for the 4-year period = 26 Million trips
* The Total Revenue generated = 387 Million dollars
* The Total Number of Passengers = 35 Million
* The Average Fare collected per trip = $12.28
* The Most Used Payment Type = Credit Card

## Relevant Links
* [Report Presentation](https://www.linkedin.com/posts/rukevweevwrujae_data-analytics-bigdata-activity-6897524091298144256-F5pG?utm_source=linkedin_share&utm_medium=member_desktop_web)
* [LinkedIn](https://www.linkedin.com/in/rukevweevwrujae/)
