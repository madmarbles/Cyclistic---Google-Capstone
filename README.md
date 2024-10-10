# Cyclistic - Google-Capstone
**Case study: How does a bike-share company navigate speedy success?**
The final capstone project for the Google Data Analytics Professional Certificate on Coursera.

## Scenario

The marketing analyst team at Cyclistic, a bike-share company in Chicago, is led by Director Lily Moreno. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes dierently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations

## Background

Cyclistic is a fictional bike-share company that was launched in Chicago of 2016. This program now owns over 5,000 bicycles and over 600 docking stations. Cyclistic is unique in that if offers bicycles that are inclusive of disabilities, including reclining bikes, hand tricycles, and cargo bikes. This makes up about 8% of riders, as most opt for traditional bikes. A majority of Cyclistic users ride for leisure, and about 30% use Cyclistic for their daily commute to work.

Multiple options are available for customers to use bikes: single-ride passes, full-day passes, and annual memberships. Annual memberships are more profitable than casual riders.

Lily Moreno, the Director of Marketing, wants to design marketing strategies that will convert casual riders to annual members. This will be done by analyzing how casual riders and annual members differ, why casual riders would buy a membership, and how digital media can affect marketing tactics. Moreno and her team will analyze historical data of Cyclistic bike trips to identify trends.

## 1. Business Task

### Project objective: 
Identify how annual members and casual riders use Cyclistic differently

### Stakeholders:
Primary: Lily Moreno, Director of Marketing
Secondary: Cyclistic Executive Team

## 2. Data Sources

### Source and Integrity
The data was accessed from a [remote server](https://divvy-tripdata.s3.amazonaws.com/index.html) and is stored in separated into monthly .csv files. The data used was provided by Motivate International Inc. under [this license](https://divvybikes.com/data-license-agreement). The license states that the data is provided “As is” as per bikeshares sole discretion. For this case study, the data will be considered first-party data from Cyclistic. The data cannot be connected to any individual riders, limiting information on whether an individual lives in the Cyclistic service area or purchased multiple single passes. 


### Preparation of Data
The dataset has individual files for each month of data. Some files exceed the limit for SQL, so data cleaning and preparation will use data from 2019 and take place in R.

#### Observations
* Each month contains thirteen columns: "ride_id”, "rideable_type", "started_at", "ended_at”, "start_station_name", "start_station_id", "end_station_name", "end_station_id", "start_lat", "start_lng”, "end_lat", "end_lng", and "member_casual”
* “started_at” and “ended_at” columns contain date-time data formatted into format YYYY-MM-DD HH:MM:SS
* “start_station_id” is not consistent in format. Some values are numeric, some begin with characters, length is variable
* Missing “end_station_name” and “end_station_id” in multiple rows

## 3. Clean and Validate Data

###Process
All code can be found [here]()

* Check column names for consistency and rename any necessary.
* Aggregate columns with similar data
* Combine the four table to one dataset
* Remove irrelevant columns
* Clean data
* Standardize date formats
* Calculate ride length
* Remove bad data
* Calculate number of weekly rides, duration of weekly rides, and average duration by season
* Create dashboards


## 4. Analyze Data

With the data cleaned and aggregated, the new dataset shows that annual members make up 76.7% of Cyclistic's total customers, and casual riders make up 23.3%. Annual members generally have a greater quantity of rides, but casual memebrs are more likely to take longer rides. All rides increase during the summer. Annual members likely ride for their commute to work, leading to an increase in rides on weekdays.

## 5. Recommendations

Cyclistic should create new plans that appeal to the needs of Casual riders. This plan would be most effective if it only included weekends over the course of a year. The weekend plan should be available at a lower price than the standard annual membership, to appeal to customers riding for leisure.
As all rides increase during the summer, it would also be beneficial to introduce a seasonal plan for all of the seasons. It can be priced at a quarter of the value of the annual membership. This will allow customers the option to try out the annual plan during a busier time and can generate more interest in the annual plan to convert casual riders to annual members.
