 ![image](https://github.com/AtilaKzlts/Snowflake-Streamlit/blob/main/assets/bar.png)


<div align="center">
  <h1>Web Development Insights: Device & Browser Performance</h1>
 </p>
</div>

 
## Table of Contents

  - Project Introduction
  - About the Data Set
  - Steps
  - Snapshot


## Project Introduction

This project is designed to help web development teams identify issues across different browsers and devices, optimize site performance, and enhance user experience. Using Google Analytics 4 (GA4) data, key metrics such as **bounce rate and average session duration** are analyzed and visualized through Looker to create a dashboard. This dashboard aims to support the development team in making data-driven decisions, gaining a deeper understanding of website performance across various devices and browsers, and implementing necessary improvements.

## About the Data Set

| **Column Name**         | **Description**                                                     |
|-------------------------|---------------------------------------------------------------------|
| `SESSIONS`             | Total number of sessions.                                         |
| `AVG_SESSION_DURATION` | Average session duration (in seconds).                           |
| `ENGAGED_SESSIONS`     | Number of engaged sessions (sessions exceeding a set threshold). |
| `BOUNCE_RATE`         | Bounce rate (`Single-page sessions / Total sessions * 100`).     |
| `DEVICE_CATEGORY`      | Category of the device used (Mobile, Tablet, Desktop, etc.).     |
| `PAGE_VIEWS`          | Total number of pages viewed by the user during a session.       |
| `OPERATING_SYSTEM`     | Operating system used by the user (Windows, iOS, Android, etc.). |
| `BROWSER`             | Browser used by the user (Chrome, Safari, Firefox, etc.).        |
| `ENGAGEMENT_RATE`      | Engagement rate (`ENGAGED_SESSIONS / SESSIONS * 100`).           |


## **Steps**  

![image](https://github.com/AtilaKzlts/Device-and-Browser-Performance-Analysis/blob/main/assets/diagram.svg)

#### **1. Data Collection**  
- Required web analytics data was retrieved from **Google Analytics 4 (GA4)** and stored in **BigQuery**.  
- The dataset included **user interactions, traffic sources, session metrics, and engagement data**.  

#### **2. Data Cleaning and Processing**  
- **Nested JSON fields** (`event_params`, `user_properties`) were **flattened** to extract structured insights from GA4’s event-based data model.  
- Missing values, duplicate records, and inconsistencies were identified and resolved to ensure data accuracy.  
- **Key performance indicators (KPIs)** were calculated using BigQuery SQL:  
  - **Engagement Rate** = `(Engaged Sessions / Total Sessions) * 100`  
  - **Bounce Rate** = `(Single Page View Sessions / Total Sessions) * 100`
  - **Engagement Rate** = (Interacted Sessions / Total Sessions) * 100

#### **3. Data Visualization and Analysis**  
- The cleaned dataset was connected to **Looker Studio** to create an **interactive dashboard**.  
- The dashboard provided insights into **traffic sources, session behaviors, device usage, and user engagement trends**.  
- **Filters and dynamic visualizations** were added to analyze trends across different time periods and user segments.  


## Snapshot 

![image](https://github.com/AtilaKzlts/Device-and-Browser-Performance-Analysis/blob/main/assets/dashsnap_1.png)


![image](https://github.com/AtilaKzlts/Device-and-Browser-Performance-Analysis/blob/main/assets/dashsnap_2.png)



### [**Return to Portfolio**](https://github.com/AtilaKzlts/Atilla-Portfolio)
