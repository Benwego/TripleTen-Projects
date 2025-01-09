# Zuber Ride-Sharing Analysis | MM/YY

### Project Overview

**Company:** Zuber (Hypothetical Company)  
**Industry:** Ride-Sharing  
**Location:** Chicago, IL  

Zuber is a new ride-sharing company looking to enter the Chicago market. As an analyst, I was tasked with analyzing historical taxi ride data to identify patterns in passenger preferences and the influence of external factors such as weather on ride frequency. You’ll also investigate how weather conditions affect the duration of rides between specific locations, such as the Loop and O'Hare International Airport. This project simulates an analysis based on available taxi ride data to guide Zuber’s strategy for optimizing its service offering.

### Data Overview

The data is contained in a relational database with the following tables:

1. **neighborhoods**: Data on city neighborhoods
   - `name`: Name of the neighborhood
   - `neighborhood_id`: Unique neighborhood code

2. **cabs**: Data on taxis
   - `cab_id`: Unique vehicle identifier
   - `vehicle_id`: Technical ID of the vehicle
   - `company_name`: Name of the taxi company

3. **trips**: Data on rides
   - `trip_id`: Unique ride code
   - `cab_id`: Code of the vehicle operating the ride
   - `start_ts`: Ride start time (rounded to the hour)
   - `end_ts`: Ride end time (rounded to the hour)
   - `duration_seconds`: Duration of the ride in seconds
   - `distance_miles`: Distance of the ride in miles
   - `pickup_location_id`: Code of the neighborhood where the ride started
   - `dropoff_location_id`: Code of the neighborhood where the ride ended

4. **weather_records**: Data on weather conditions
   - `record_id`: Unique weather record code
   - `ts`: Date and time when the weather record was taken
   - `temperature`: Temperature at the time of the record
   - `description`: Weather description (e.g., "light rain", "scattered clouds")

### Project Goals

1. **Exploratory Data Analysis (EDA)**:  
   Perform an in-depth analysis of ride frequency patterns, particularly focusing on the number of rides by different taxi companies in Chicago over specified time periods (November 2017). Key tasks:
   - Identify ride frequency by taxi company for specific dates.
   - Examine ride frequency for companies with names containing “Yellow” or “Blue”.
   - Group and aggregate ride counts for popular companies like Flash Cab and Taxi Affiliation Services.

2. **Weather Impact Analysis**:  
   Investigate the effect of weather conditions, specifically rain, on ride durations from the Loop to O'Hare International Airport:
   - Identify weather conditions (rainy vs. non-rainy days) for each hour using the `weather_records` table.
   - Analyze how the duration of rides from the Loop (neighborhood_id: 50) to O'Hare (neighborhood_id: 63) differs on rainy Saturdays compared to other days of the week and different weather conditions.

### Steps to Complete the Project

#### **Step 1: Exploratory Data Analysis**
- **Task 1**: Find the number of taxi rides for each taxi company for November 15-16, 2017, and name the resulting field `trips_amount`. Sort by `trips_amount` in descending order.
- **Task 2**: Find the number of rides for taxi companies containing the words "Yellow" or "Blue" for November 1-7, 2017. Name the resulting field `trips_amount` and group by `company_name`.
- **Task 3**: Group the taxi companies Flash Cab and Taxi Affiliation Services and aggregate the number of rides for each. Name the resulting field `trips_amount`. All other companies should be grouped under the label "Other".

#### **Step 2: Weather Impact on Ride Duration**
- **Task 1**: Retrieve the neighborhood identifiers for the Loop and O'Hare from the `neighborhoods` table.
- **Task 2**: Use the `CASE` operator to classify each hour as "Bad" (if the description contains rain or storm) or "Good" for other conditions. Create the field `weather_conditions` based on this classification.
- **Task 3**: Retrieve all rides from the Loop (neighborhood_id: 50) to O'Hare (neighborhood_id: 63) on Saturdays. Retrieve their duration and weather conditions for each ride. Use the weather classification from the previous task to add the `weather_conditions` field. Analyze the results to determine how weather (especially rain) affects ride durations.

### Key Findings

- **Popular Taxi Companies**: Based on the data analysis, identify which companies are most popular during specific periods, such as November 2017. This helps Zuber understand which competitors it may be up against in terms of market share.
- **Weather and Ride Duration**: Analyze how weather (e.g., rain) impacts ride times between key locations like the Loop and O'Hare, which could inform Zuber's operational strategy during adverse weather conditions.

### Tools and Technologies

- **Database Management**: SQL (Structured Query Language) for querying and aggregating data from the relational database.
- **Data Analysis**: SQL JOIN operations to link the `trips` table with the `weather_records` table using the timestamps (`start_ts` and `ts`).
- **Data Aggregation**: GROUP BY and CASE statements to categorize and analyze the data.

### Hypothetical Scenario Disclaimer

This project is based on a hypothetical scenario for a new ride-sharing company, Zuber. The data used is also hypothetical and not based on real-world taxi ride data. All findings and conclusions are drawn from the data provided for this exercise and are meant solely for educational purposes.

---

### Project Deliverables

1. **SQL Queries**: All SQL queries used to extract, clean, and analyze the data.
2. **Reports and Analysis**: Insights on taxi company performance, the impact of weather on ride durations, and key recommendations for Zuber’s operational strategies.
3. **Visualizations**: If applicable, visual representations of the data, including charts or graphs to support the analysis.

Good luck with the analysis, and remember to keep the data interpretations consistent with the hypothetical nature of this project!

