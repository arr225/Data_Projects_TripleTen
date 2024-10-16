# Data Analysis and Hypothesis Testing for Rideshare Company

### [Link to the Project](https://github.com/arr225/Data_Projects_TripleTen/blob/0fe5dafc705a51bf9c487958a95995bb88cdfdae/Data%20Analysis%20and%20Hypothesis%20Testing/Data%20Analysis%20and%20Hypothesis%20Testing%20for%20Rideshare%20Company.ipynb)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset and Features](#dataset-and-features)
3. [Methodology](#methodology)
4. [Visuals](#visuals)
5. [Results](#results)
6. [Suggestions for Improvement](#suggestions-for-improvement)

---

## Project Overview
In this project, I worked as an analyst for Zuber, a new ride-sharing company launching in Chicago. The main goal was to explore the available data, identify passenger patterns, and investigate the impact of weather on ride frequency. This analysis would help Zuber understand factors that influence rides and help them strategize for better service.

**Project Goals:**
- Identify patterns in ride-sharing data.
- Understand the impact of weather conditions on ride frequency.
- Test hypotheses regarding the duration of rides in specific conditions.

---

## Dataset and Features
The project used a comprehensive database of Chicago taxi rides, including the following tables:

**Neighborhoods Table:**
- `name`: Name of the neighborhood
- `neighborhood_id`: Neighborhood code

**Cabs Table:**
- `cab_id`: Vehicle code
- `vehicle_id`: Technical ID of the vehicle
- `company_name`: Name of the company that owns the taxi

**Trips Table:**
- `trip_id`: Unique ride code
- `cab_id`: Vehicle ID
- `start_ts`: Start time of the ride
- `end_ts`: End time of the ride
- `duration_seconds`: Duration of the ride in seconds
- `distance_miles`: Distance covered during the ride
- `pickup_location_id`: Pickup neighborhood ID
- `dropoff_location_id`: Dropoff neighborhood ID

**Weather Records Table:**
- `record_id`: Record code
- `ts`: Date and time of the weather record
- `temperature`: Temperature at the time of the record
- `description`: Weather conditions (e.g., "light rain", "scattered clouds")

---

## Methodology
1. **Step 1: Parsing Weather Data**
   - Weather data from Chicago in November 2017 was parsed from a website and added to the existing dataset.

2. **Step 2: Exploratory Data Analysis**
   - Analyzed the number of rides for each taxi company during November 15-16, 2017.
   - Filtered the data for taxi companies with names containing "Yellow" or "Blue" to find their ride numbers between November 1-7, 2017.
   - Compared ride frequencies across popular taxi companies Flash Cab and Taxi Affiliation Services, grouping all others under "Other."

3. **Step 3: Hypothesis Testing**
   - Investigated the hypothesis: "The average duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays."
   - This step involved:
     - Retrieving identifiers for O'Hare and Loop neighborhoods.
     - Grouping weather conditions as "Bad" (rain, storm) or "Good".
     - Examining ride durations from the Loop to O'Hare on Saturdays under different weather conditions.
   
4. **Step 4: Data Analysis with Python**
   - Analyzed two additional datasets: 
     - **project_sql_result_01.csv**: Contains company names and the number of rides per taxi company on specific dates.
     - **project_sql_result_04.csv**: Contains the names of Chicago neighborhoods and the average number of rides ending in each neighborhood in November 2017.
   - Visualized data for taxi companies and the top 10 neighborhoods based on the number of drop-offs.

---

## Visuals

### Taxi Companies and Number of Rides
![Taxi Companies and Rides](https://github.com/arr225/Data_Projects_TripleTen/blob/35ef401dd684ddc8f8ca8dc0a08e237ef1706bfa/Data%20Analysis%20and%20Hypothesis%20Testing/Taxi%20Companies%20and%20Number%20of%20Rides.png)

*Description*: This bar graph displays the number of rides taken with different taxi companies in Chicago, highlighting the most popular companies during the analysis period. The companies are listed in descending order based on the number of rides, with Flash Cab and Taxi Affiliation Services leading the count.

### Top 10 Neighborhoods by Drop-offs
![Top 10 Neighborhoods](https://github.com/arr225/Data_Projects_TripleTen/blob/8849f60cd59205f489c849a2b614efd34c951abc/Data%20Analysis%20and%20Hypothesis%20Testing/Top%2010%20Neighborhoods%20by%20Drop-offs.png)

*Description*: This bar graph highlights the top 10 neighborhoods in Chicago by the average number of taxi drop-offs. The Loop neighborhood leads with the highest number of drop-offs, followed by River North and Streeterville. This analysis provides insights into the most frequented areas for taxi rides during the evaluation period, showcasing the demand for transportation services in these key locations.

### Ride Duration and Weather Conditions
![Ride Duration](https://github.com/arr225/Data_Projects_TripleTen/blob/800d1efb1ae14666511e4fd90af676255e8eb232/Data%20Analysis%20and%20Hypothesis%20Testing/Ride%20Duration%20and%20Weather%20Conditions.png)

*Description*: This histogram illustrates the distribution of ride durations on rainy and non-rainy Saturdays. The graph shows that the majority of rides on both rainy and non-rainy Saturdays lasted between 1000 and 3000 seconds, with rainy Saturdays (highlighted in blue) having a more condensed distribution. The comparison of these two conditions provides insights into how weather impacts ride durations, particularly on rainy days.

---

## Results
- The analysis revealed patterns in the taxi data that aligned with external factors such as company affiliation and weather conditions.
- The hypothesis test suggested that weather conditions do have an impact on ride durations, with significant differences observed on rainy Saturdays.

---

## Suggestions for Improvement
- **Further Data Collection**: Integrating more detailed weather data over a longer period could refine the impact analysis.
- **Ride Optimization**: Zuber could use the insights about weather impacts to adjust driver availability and pricing models.
- **Passenger Preferences**: Collecting more information on passenger demographics and preferences could help Zuber tailor services and marketing strategies.
