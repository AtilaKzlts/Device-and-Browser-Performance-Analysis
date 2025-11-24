

![image](https://github.com/AtilaKzlts/Device-and-Browser-Performance-Analysis/blob/main/assets/diagram.svg)

<div align="center">
  <h1>Web Development Insights: Device & Browser Performance</h1>
 </p>
</div>

 
## ▌ Table of Contents

  - Project Introduction
  - Executive Summary
  - About the Data Set
  - Steps
  - Snapshot


## ▌ Project Introduction

This project is designed to help web development teams identify issues across different browsers and devices, optimize site performance, and enhance user experience. Using Google Analytics 4 (GA4) data, key metrics such as **bounce rate and average session duration** are analyzed and visualized through Looker to create a dashboard. This dashboard aims to support the development team in making data-driven decisions, gaining a deeper understanding of website performance across various devices and browsers, and implementing necessary improvements.

## ▌ Executive Summary


| Analysis Area / Phase | Insight (Key Finding) | Recommended Action |
| :--- | :--- | :--- |
| **Device Strategy & UX** | **Desktop Dominance:** Over 75% of views come from Desktop (especially Mac & Chrome). The user base is in a "work mode" or deep research context, rather than casual mobile browsing. | **Primary Optimization:** Ensure the Desktop UI (particularly for Chrome/Mac) is flawless. Avoid compromising complex desktop features for mobile responsiveness unless mobile traffic increases substantially. |
| **Browser Performance (Friction)** | **The "Samsung" Anomaly:** While Chrome users stay for ~4:45 min, **Samsung Internet** users drop to ~1:19 min. This indicates a specific technical rendering bug or broken layout unique to Samsung devices. | **Tech Debt Investigation:** Assign a frontend developer to debug the site specifically on Samsung Internet browsers. Check for broken JavaScript or layout shifts causing premature exits. |
| **Platform Engagement** | **Operating System Split:** Macintosh (96K) nearly doubles Windows (53K). High iOS usage suggests a "premium" or tech-savvy demographic. | **Targeting Strategy:** If running paid ads (Google/Meta), aggressively bid on the Apple ecosystem (Mac and iOS) users, as they represent the most engaged core audience. |
| **Data Integrity (Edge Cases)** | **Misleading Bounce Rates:** The table shows 100% Bounce Rates for niche browsers (e.g., Meta Quest, Firefox Tablet). These are statistically insignificant, low-volume edge cases. | **Data Cleaning:** To avoid "False Alarm" reporting, filter out browser/device combinations with <50 Sessions before calculating Bounce Rate. Focus on high-volume problems, not low-volume noise. |
| **Conversion Funnel** | **Visual and Conversion Focus:** Desktop (56%) performance is significantly better than Mobile (51%). The funnel visualization is misleading, as it compares categories, not sequential steps. | **Conversion Focus:** Since Desktop drives volume AND better conversion, prioritize the implementation of desktop-specific, high-value conversion elements (e.g., sticky sidebars, targeted modals) to push the rate from 56% to 60%+. |





## ▌ About the Data Set

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



## ▌ **Steps**  



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
