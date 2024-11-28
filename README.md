Hotel Booking Exploratory Data Analysis (EDA) Project
Overview
This project focuses on exploring and analyzing a dataset related to hotel bookings. The dataset includes two types of hotels—City Hotel and Resort Hotel—and contains various details about bookings, customer demographics, and stay patterns. By performing data cleaning, manipulation, and visualization, we identified key insights that can inform business strategies and improve hotel performance.

Objectives
Understand the Dataset:

Explore the structure and details of the dataset.
Handle missing and duplicate data for cleaner analysis.
Data Cleaning and Transformation:

Identify and correct data inconsistencies.
Create new calculated columns to enhance data usability.
Exploratory Data Analysis (EDA):

Generate meaningful visualizations to uncover patterns and trends.
Highlight critical insights into customer preferences, booking patterns, and potential business opportunities.
Dataset
Summary:
Rows: 119,390
Columns: 32
Data Types:
Object (categorical features)
Float64 (continuous numerical features)
Int64 (discrete numerical features)
Key Features:
Hotel: Type of hotel (City or Resort).
Is_Canceled: Whether the booking was canceled.
Lead_Time: Number of days between booking and arrival.
Adults, Children, Babies: Number of guests per booking.
Reservation_Status_Date: Date when the reservation status was updated.
Issues Identified:
Missing Values:
Significant missing values in columns like Company (112,593), Agent, and Country.
Minimal missing values in Children (4).
Duplicates:
31,994 duplicate rows identified and removed.
Inconsistent Data:
Rows where the combined number of adults, children, and babies was 0, indicating no guests or bookings.
Methodology
1. Data Collection
Initial exploration of the dataset using:
head(), tail(), info(), describe(), columns()
Generated a list of unique values for each column to understand data diversity.
2. Data Cleaning and Manipulation
Handling Missing Values:
Filled missing values in relevant columns using appropriate strategies (e.g., fillna()).
Dropped Duplicates:
Removed 31,994 duplicate rows.
Removing Invalid Rows:
Dropped rows where Adults + Children + Babies = 0.
Data Type Conversion:
Changed reservation_status_date from object to datetime.
New Calculated Columns:
total_people: Sum of Adults, Children, and Babies.
total_stay: Sum of stays_in_week_nights and stays_in_weekend_nights.
3. Data Visualization
Visualization Goals:

Understand booking trends over time.
Analyze cancellation rates and guest demographics.
Explore customer preferences for City vs. Resort hotels.
Identify seasonal and yearly booking patterns.
Techniques and Tools:

Used libraries like Matplotlib and Seaborn for visualization.
Visualized data using bar charts, line graphs, and heatmaps to derive actionable insights.
Insights and Findings
1. Data Distribution:
City Hotels have more bookings than Resort Hotels.
Significant proportion of bookings had missing or undefined values for certain fields like Company.
2. Cancellation Patterns:
A notable percentage of bookings were canceled, especially for City Hotels.
3. Guest Trends:
Rows where the number of guests (Adults + Children + Babies) was 0 were removed, as they represented invalid bookings.
4. Seasonal and Yearly Trends:
Bookings peak during specific months, indicating seasonal demand.
5. Business Implications:
Insights into customer behavior can help optimize marketing campaigns and improve guest retention strategies.
