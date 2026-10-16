<img width="1421" height="471" alt="image" src="https://github.com/user-attachments/assets/836dc535-85a3-478b-9810-c210c7b3cfd1" />

FitTrack 360 — Fitness Intelligence Dashboard

An interactive **Power BI fitness analytics dashboard** built using Fitbit data to analyze physical activity, sleep, heart rate, weight, and BMI patterns.


 📌 Project Overview

**FitTrack 360** transforms raw Fitbit data into an interactive Business Intelligence dashboard using **Power BI**.

The project combines multiple fitness datasets and organizes them into a structured analytical data model. It uses **Power Query** for data preparation, **DAX** for analytical calculations, and interactive visualizations to explore fitness and health-related patterns.

The dashboard is designed to help users understand activity levels, sleep behavior, heart-rate patterns, and weight-related trends through KPIs, comparisons, trends, and interactive filtering.


 🎯 Project Objectives

The main objectives of this project are to:

- Analyze daily and hourly physical activity patterns
- Track steps, calories, distance, and active minutes
- Analyze sleep duration and sleep efficiency
- Explore heart-rate patterns throughout the day
- Analyze weight and BMI trends
- Compare activity patterns across users and activity segments
- Explore relationships between fitness and health metrics
- Build an interactive and user-friendly Power BI dashboard

 📊 Dashboard Pages

 1. Fitness Overview

Provides a high-level summary of overall fitness activity.

 Key KPIs
- Average Daily Steps
- Average Daily Calories
- Average Sleep Duration
- Average Resting Heart Rate

Analysis
- Fitness trends over time
- Activity level distribution
- Average steps by day of week
- Top 5 active users



 2. Activity & Fitness Analytics

Focuses on physical activity and movement patterns.

 Key KPIs
- Average Daily Steps
- Total Distance
- Average Daily Calories
- Active Minutes

Analysis
- Steps by Hour of Day
- Activity Intensity by Day and Hour
- Calories Burned by Activity Segment
- Active Minutes by Intensity
- Steps vs Calories

This page helps identify when users are most active and how activity relates to calorie expenditure.



 3. Sleep & Recovery Analytics

Focuses on sleep behavior and recovery patterns.

Key KPIs
- Average Sleep Duration
- Average Sleep Efficiency
- Average Time in Bed
- Sleep Debt

Analysis
- Sleep Duration & Efficiency Trend
- Sleep Composition
- Average Sleep Duration by Day of Week
- Sleep vs Activity by User
- Users by Sleep Efficiency

This page helps explore differences in sleep patterns and their relationship with physical activity.



 4. Heart Rate & Health Analytics

Analyzes heart-rate, weight, and BMI patterns.

### Key KPIs
- Average Resting Heart Rate
- Maximum Heart Rate
- Average Weight
- Average BMI

Analysis
- Heart Rate Trend Over Time
- Heart Rate by Time of Day
- Weight Trend Over Time
- Average BMI by Activity Segment
- Heart Rate vs Steps



 🧩 Data Model

The project uses a structured **fact and dimension data model**.

 Dimension Tables

**dim_date**
- Date
- DateKey
- Day
- Month
- Month Number
- Weekday
- Weekday Number
- Week Number
- Year
- IsWeekend

dim_user
- UserKey
- UserLabel
- ActivitySegment
- Average Daily Steps
- Sleep Availability
- Heart Rate Availability
- Weight Availability

 Fact Tables

fact_daily_activity
- Daily activity and fitness measurements

fact_hourly_steps
- Hourly step-level activity data

fact_sleep_day
- Daily sleep measurements

fact_sleep_session
- Sleep-session-level information

fact_heartrate_minute
- Minute-level heart-rate observations

fact_weight
- Weight-related measurements

 Measures Table

_Measures

A dedicated table used to organize DAX measures used throughout the dashboard.



🔑 Data Relationships

The model uses common keys to connect the tables.

DateKey

Connects the `dim_date` table with relevant fact tables and enables consistent time-based analysis.

### UserKey

Connects the `dim_user` table with fact tables and enables user-level analysis.

The dimensional structure allows filters such as user, date, weekday, and activity segment to dynamically affect the dashboard.



🔄 Data Preparation

Power Query was used to prepare the data before analysis.

The workflow included:

1. Loading the source datasets
2. Cleaning and organizing the data
3. Standardizing data types
4. Preparing required fields
5. Creating and preparing keys
6. Structuring the datasets
7. Loading the prepared data into the Power BI model

Overall Workflow

text
Raw Fitbit Data
      ↓  
Power Query
      ↓ 
Data Cleaning & Transformation
      ↓ 
Data Modeling
      ↓  
Relationships
      ↓  
DAX Measures
      ↓ 
Visualizations
      ↓
Interactive Dashboard
