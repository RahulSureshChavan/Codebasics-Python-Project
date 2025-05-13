# Exploratory Data Analysis (EDA) in the Hospitality Domain using Python (Pandas)
## Project Overview
This project is an exploratory data analysis (EDA) exercise focused on hospitality domain data. It is part of the Data Analytics Bootcamp by Codebasics. The goal is to analyze hotel bookings data using Python (Pandas) and extract meaningful insights to help business decision-making.

Business Problem
AtliQ Grands, a hotel chain in India, is facing declining market share and revenue due to increasing competition. To make informed decisions, the management has hired a data analytics team to analyze booking data and identify opportunities for revenue growth.

Data Source & ETL Process
Bookings data is stored in a transactional database. However, querying over this live database could impact operations negatively. Therefore, an ETL process is performed to extract, transform, and load the data into a Data Warehouse. Analysts work with cleaned and structured data from the Data Warehouse for insights.

Dataset Description
The following CSV files, extracted from the Data Warehouse, serve as the basis for analysis:

dim_date.csv: Contains date-related attributes such as week number and whether the day is a weekday or weekend.

dim_hotels.csv: Details of hotels, including property_id, category, and location.

dim_rooms.csv: Room details, categorized by class (Standard, Elite, Premium, Presidential).

fact_aggregated_bookings.csv: Aggregated booking and capacity data.

fact_bookings.csv: Detailed transaction data of individual bookings.

new_data_august.csv: Newly collected booking data for August.

Project Steps
This project follows a structured approach:

Understanding the Business Problem – Define objectives and key questions.

Data Collection & Understanding – Explore available datasets.

Data Cleaning & Exploration – Remove inconsistencies, handle null values, and detect outliers.

Data Transformation – Compute additional metrics and enrich datasets.

Insights Generation – Perform ad-hoc analysis to derive business insights.

Exploratory Data Analysis (EDA)
Data Exploration
Load CSV files into Pandas DataFrames.

Explore fact_bookings dataset to identify:

Number of records (rows & columns).

Unique room categories.

Booking platforms and their contributions.

Statistics of numerical columns.

Analyze dim_hotels dataset:

Number of hotels per category and city.

Visualize hotel distribution across cities using bar charts.

Answer business questions:

Identify unique property_id values in aggregated bookings dataset.

Compute total bookings per property.

Determine days when bookings exceeded hotel capacity.

Identify properties with the highest capacity.

Data Cleaning
Handling Negative Guest Entries: Remove entries where guest count is negative.

Detecting Revenue Outliers: Use a 3-standard deviation method to define upper and lower limits for revenue, filtering out extreme values.

Managing Null Values: Ignore null values in ratings_given column as they don’t impact analysis.

Null Value Treatment: Identify missing values in aggregate bookings and fill them with appropriate substitutes such as mean or median.

Data Transformation
Calculating Occupancy Percentage: Compute occupancy percentage (successful bookings / capacity).

Data Formatting: Multiply occupancy percentage by 100 and round values to 2 decimal places for better readability.

Insights Generation
This phase answers key business questions using groupby(), merge(), drop(), concat(), info(), to_datetime() functions in Pandas.

Key Findings:
Average occupancy rate per room category – Understand booking efficiency across room types.

City-wise occupancy rates – Identify trends for different cities.

Weekday vs. Weekend occupancy comparison – Determine peak booking times.

Monthly city-wise occupancy analysis – Evaluate how demand varies across months.

Revenue insights:

Total revenue per city.

Month-by-month revenue trends.

Revenue distribution across hotel categories.

Pie chart visualization of revenue from different booking platforms.

Customer ratings analysis – Determine average rating per city to gauge customer satisfaction.

Conclusion
This project successfully leverages Pandas for structured Exploratory Data Analysis on hotel bookings data. The findings from this analysis provide actionable insights that can help AtliQ Grands optimize pricing, manage inventory, and improve customer engagement. The structured workflow—from data cleaning to insights generation—showcases how data analytics can drive business decisions effectively.
