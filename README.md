# Uber and Lyft Dataset Analysis - Boston, MA

## Overview

This project involves the analysis of Uber and Lyft rides in Boston, MA, using a dataset consisting of 693,071 rides that took place between November 26th, 2018, and December 18th, 2018. The dataset includes 57 variables such as ride type, ride distance, ride price, weather conditions, and timestamps, offering an extensive foundation for analysis.

The goal of this project is to explore the dataset through dimensional modeling and answer key business questions related to surge pricing, ride types, and driver-ride cost comparisons.

## Dataset Description

- **Size**: 367.38 MB
- **Variables**: 57
- **Attributes**:
  - Ride type, distance, price, weather conditions, ride timestamps, source and destination locations, and more.
  
The dataset is sourced from Kaggle, uploaded by Bikram Maharjan, a data science master's student. You can download the dataset in CSV format and find additional information about each field at the Kaggle page [here](https://www.kaggle.com/datasets/brllrb/uber-and-lyft-dataset-boston-ma).

## ETL Process

### Data Cleaning

The initial step involved cleaning the dataset to ensure quality and remove unnecessary attributes. The primary focus was on:
- Removing missing or irrelevant data.
- Filtering out outliers.
- Standardizing attribute formats.

### Data Transformation

After the cleaning process, the dataset was transformed into structured tables for further analysis:
1. **Fact Table: `fact_rides`**: Core metrics of ride-sharing events.
2. **Dimension Tables**:
   - **dim_time**: Temporal information.
   - **dim_location**: Source and destination ride details.
   - **dim_ride_type**: Categorization of ride types.
   - **dim_weather**: Weather information during the ride.

### Data Loading

The cleaned and transformed data was loaded into the respective tables. This structured dataset formed the foundation for answering key business questions.

---

## Business Questions & Insights

### Business Question 1: Surge Pricing and Driver Availability

**Question**: Which locations could benefit from an increased number of drivers to capture all ridership demand, and at what hours is this increased supply most needed?

**Insights**:
- **Peak Surge Times**: Surge pricing is most frequent between 11 PM-1 AM, 8 AM-9 AM, and 1 PM.
- **Locations with High Surge**:
  - **Fenway**: Surge is highest at Hour 0 (Late-night activity).
  - **Theatre District**: Surge is highest at Hour 8 (Morning demand).
  - **Back Bay**: Surge is significant during hours 9 and 13 (Midday and morning).
  - **Northeastern University**: Surge is highest during late-night hours (1 AM and 11 AM).

**Recommendation**: To reduce surge pricing, rideshare companies should incentivize drivers to be available in high-demand areas at peak times. For instance, during major events like baseball games at Fenway, offering guaranteed earnings could help manage the demand.

---

### Business Question 2: Popular Ride Types in Different Locations

**Question**: What is the most popular ride type (e.g., luxury, shared, etc.) in each specific location, and how can this insight inform targeted promotional strategies?

**Insights**:
- **Back Bay**: 
  - Most popular Uber ride type: WAV (Accessible rides).
  - Most popular Lyft ride type: Lux (Premium, comfortable rides).
- **Fenway**: 
  - Most popular Uber ride type: WAV (Accessibility need).
  - Most popular Lyft ride type: Lux (Premium rides).
- **Financial District**:
  - Most popular Uber ride type: UberPool (Shared rides, cost-conscious commuters).
  - Most popular Lyft ride type: Lux Black (Premium rides).
  
**Recommendation**: Increase availability of accessible rides (WAV) in locations like Back Bay, Fenway, and North Station. Promote premium services like Lux Black in business-heavy areas and consider targeted promotions for specific ride types.

---

### Business Question 3: Ride Cost and Earnings Potential

**Question**: Which cab service (e.g., Lyft or Uber) offers the highest costs for riders and the greatest earning potential for drivers across different locations, and how does this affect the number of rides?

**Insights**:
- **Average Ride Costs**: Lyft drivers earn more per mile and charge higher fares.
- **Ride Volume**: Despite the higher fares and earnings for Lyft, Uber maintains a higher ride volume, indicating that affordability drives demand.
  
**Recommendation**: Lyft should emphasize its premium service quality and improve service reliability, especially in high-demand areas like Fenway and Haymarket Square. On the other hand, Uber could focus on affordability in residential and commuter-heavy areas to maintain its ride volume.

---

## Conclusion

This project demonstrates the potential of data analysis in the ridesharing industry. By answering business questions about surge pricing, popular ride types, and ride costs, we provide actionable insights that can be used to optimize driver availability, improve promotional strategies, and enhance customer satisfaction.

---
