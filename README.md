# Exploratory Data Analysis (EDA) in the Hospitality Domain using Python (Pandas)
## Project Overview
This project is an exploratory data analysis (EDA) exercise focused on hospitality domain data. It is part of the Data Analytics Bootcamp by Codebasics. The goal is to analyze hotel bookings data using Python (Pandas) and extract meaningful insights to help business decision-making.

## Business Problem
AtliQ Grands, a hotel chain in India, is facing declining market share and revenue due to increasing competition. To make informed decisions, the management has hired a data analytics team to analyze booking data and identify opportunities for revenue growth.

## Data Source & ETL Process
Bookings data is stored in a transactional database. However, querying over this live database could impact operations negatively. Therefore, an ETL process is performed to extract, transform, and load the data into a Data Warehouse. Analysts work with cleaned and structured data from the Data Warehouse for insights.

## Dataset Description
The following CSV files, extracted from the Data Warehouse, serve as the basis for analysis:  
1. dim_date.csv: Contains date-related attributes such as week number and whether the day is a weekday or weekend.
2. dim_hotels.csv: Details of hotels, including property_id, category, and location.
3. dim_rooms.csv: Room details, categorized by class (Standard, Elite, Premium, Presidential).
4. fact_aggregated_bookings.csv: Aggregated booking and capacity data.
5. fact_bookings.csv: Detailed transaction data of individual bookings.
6. new_data_august.csv: Newly collected booking data for August.

## Project Steps
This project follows a structured approach:  
1. Understanding the Business Problem – Define objectives and key questions.
2. Data Collection & Understanding – Explore available datasets.
3. Data Cleaning & Exploration – Remove inconsistencies, handle null values, and detect outliers.
4. Data Transformation – Compute additional metrics and enrich datasets.
5. Insights Generation – Perform ad-hoc analysis to derive business insights.

## Data Exploration
1. Load CSV files into Pandas DataFrames.
2. Explore fact_bookings dataset to identify:
Number of records (rows & columns).
Unique room categories.
Booking platforms and their contributions.
Statistics of numerical columns.
3. Analyze dim_hotels dataset:
Number of hotels per category and city.
Visualize hotel distribution across cities using bar charts.
4. Answer business questions:
Identify unique property_id values in aggregated bookings dataset.
Compute total bookings per property.
Determine days when bookings exceeded hotel capacity.
Identify properties with the highest capacity.

## Data Cleaning
1. Handling Negative Guest Entries: Remove entries where guest count is negative.
2. Detecting Revenue Outliers: Use a 3-standard deviation method to define upper and lower limits for revenue, filtering out extreme values.
3. Managing Null Values: Ignore null values in ratings_given column as they don’t impact analysis.
4. Null Value Treatment: Identify missing values in aggregate bookings and fill them with appropriate substitutes such as mean or median.

## Data Transformation
1. Calculating Occupancy Percentage: Compute occupancy percentage (successful bookings / capacity).
2. Data Formatting: Multiply occupancy percentage by 100 and round values to 2 decimal places for better readability.

## Insights Generation
This phase answers key business questions using groupby(), merge(), drop(), concat(), info(), to_datetime() functions in Pandas.
Key Findings:
1. Average occupancy rate per room category – Understand booking efficiency across room types.
2. City-wise occupancy rates – Identify trends for different cities.
3. Weekday vs. Weekend occupancy comparison – Determine peak booking times.
4. Monthly city-wise occupancy analysis – Evaluate how demand varies across months.
5. Revenue insights:
Total revenue per city.
Month-by-month revenue trends.
Revenue distribution across hotel categories.
Pie chart visualization of revenue from different booking platforms.
6. Customer ratings analysis – Determine average rating per city to gauge customer satisfaction.

## Insights in Numbers
1. Occupancy Rates: Delhi had the highest occupancy (61%), Bangalore the lowest (56%).
2. Weekday vs. Weekend Demand: Weekdays averaged 51% occupancy, while weekends surged to 72%.
3. Revenue Trends: May 2022 generated the highest revenue (581M INR), while June 2022 had the lowest (553M INR).
4. Booking Source Contribution: Third-party platforms accounted for 41% of total revenue.
5. Top Earning Cities: Mumbai led with 668M INR, while Delhi had the lowest at 294M INR.
6. Hotel Category Insights: AtliQ Exotica generated the highest revenue (320M INR), while AtliQ Seasons earned the least (66M INR).

## Conclusion
This project successfully leverages Pandas for structured Exploratory Data Analysis on hotel bookings data. The findings from this analysis provide actionable insights that can help AtliQ Grands optimize pricing, manage inventory, and improve customer engagement. The structured workflow—from data cleaning to insights generation—showcases how data analytics can drive business decisions effectively.
