# Zuber Ride-Sharing Data Analysis

## Project Overview

I worked as an analyst for **Zuber**, a fictional new ride-sharing company launching in Chicago. My primary objective was to analyze and find patterns in existing taxi ride data to better understand passenger behavior, identify trends, and assess external factors, such as weather, on ride frequency.

In this project, I worked with a database containing ride information, including taxi company details, ride durations, distances, and weather conditions. The main task is to explore the data, test hypotheses, and derive actionable insights that could benefit Zuber's operations.
Project Link: https://docs.google.com/document/d/1-kx-SSolP2sOxPBboCouvk2BG3JIExrKfV4vBWBioN0/edit?usp=sharing

## Description of the Data

The database consists of the following tables:

1. **neighborhoods table**: Contains data on city neighborhoods.
   - `name`: Name of the neighborhood.
   - `neighborhood_id`: Unique identifier for the neighborhood.

2. **cabs table**: Contains data on taxis.
   - `cab_id`: Unique identifier for the vehicle.
   - `vehicle_id`: The technical ID of the vehicle.
   - `company_name`: The company that owns the vehicle.

3. **trips table**: Contains data on taxi rides.
   - `trip_id`: Unique identifier for the ride.
   - `cab_id`: The ID of the vehicle operating the ride.
   - `start_ts`: Start date and time of the ride (rounded to the nearest hour).
   - `end_ts`: End date and time of the ride (rounded to the nearest hour).
   - `duration_seconds`: Duration of the ride in seconds.
   - `distance_miles`: Distance of the ride in miles.
   - `pickup_location_id`: Neighborhood code where the ride started.
   - `dropoff_location_id`: Neighborhood code where the ride ended.

4. **weather_records table**: Contains weather information at the time of the rides.
   - `record_id`: Unique identifier for the weather record.
   - `ts`: Date and time of the weather record (rounded to the nearest hour).
   - `temperature`: Temperature at the time of the record.
   - `description`: Brief description of the weather conditions (e.g., "light rain", "scattered clouds").

## Requirements

1. **SQL Queries**: You will need to write SQL queries to retrieve and analyze specific information from the tables:
    - Count taxi rides for each taxi company for specific dates (e.g., November 15-16, 2017).
    - Filter rides for taxi companies with "Yellow" or "Blue" in their names.
    - Aggregate data by grouping certain taxi companies (e.g., Flash Cab and Taxi Affiliation Services) and label all others as "Other."
    - Retrieve weather conditions and classify them as "Bad" (rainy or stormy weather) or "Good" (other weather).

2. **Data Analysis**:
    - You will conduct exploratory data analysis (EDA) on the ride data, focusing on trends and patterns in ride frequency, taxi company performance, and the impact of weather on ride demand.
    - The analysis should cover specific periods (e.g., November 2017) and consider variables like ride duration, distance, and weather conditions.

3. **Visualizations** (Optional): Create visual representations of key insights, such as ride distribution by company, ride durations under different weather conditions, etc.

## Instructions

### Step 1: Exploratory Data Analysis

1. **Find the number of taxi rides for each taxi company for November 15-16, 2017**.
   - Sort by the number of trips (trips_amount).
   
2. **Find the number of rides for taxi companies with names containing "Yellow" or "Blue" between November 1-7, 2017**.
   - Group the results by the company name.

3. **Aggregate rides for Flash Cab and Taxi Affiliation Services** and label all other companies as "Other" for November 1-7, 2017.
   - Sort the results by trips amount.

### Step 2: Analyze the Impact of Weather on Ride Duration

1. **Retrieve the identifiers of O'Hare and Loop neighborhoods** (O'Hare: 63, Loop: 50).
   
2. **Classify weather conditions as "Bad" or "Good"** for each hour, based on the description field (e.g., "rain" or "storm" = "Bad", others = "Good").

3. **Retrieve rides from the Loop to O'Hare on Saturdays**, including weather conditions and ride duration.
   - Filter out rides with no weather data.
   - Compare ride durations for rainy vs. non-rainy Saturdays.


