🏨 AtliQ Hospitality Revenue & Operational Analytics Dashboard
An interactive Power BI Business Intelligence solution designed to analyze revenue performance, occupancy rates, and booking channel dynamics for a multi-city hotel chain in India.
📌 Project Overview
AtliQ Grands, a luxury and business hotel chain in India, is facing market share loss and declining revenue due to strategic competitive moves and inefficient operational decision-making.
This project delivers an executive-level Power BI Dashboard that processes historical transactional logs and booking records across May, June, and July to provide actionable intelligence on RevPAR, ADR, Occupancy %, and Realization Rates.
<img width="780" height="446" alt="image" src="https://github.com/user-attachments/assets/4635459f-cbc1-4888-9639-d4722cba475c" />

📊 Key Dashboard Insights & Features
Executive KPI Suite: Quick insight into core metrics—Total Revenue (₹1.69Bn), Occupancy Rate (57.79%), RevPAR (₹7.34K), ADR (₹12.70K), and Realization % (80.18%) with Week-over-Week (WoW) indicators.
Category Breakdown: Donut chart showing revenue distribution between Luxury (61.62%) and Business (38.38%) hotel segments.
Weekly Trend Analysis: Line charts mapping performance metrics across weeks 19 to 31.
Day-Type Performance Matrix: Comparative breakdown of operational performance across Weekdays vs. Weekends.
Channel Mix Performance: Dual-axis chart highlighting realization efficiency and pricing across booking platforms (Direct Online, MakeMyTrip, Journey, LogTrip, etc.).
Property Level Matrix: Detailed tabular view tracking individual hotel properties by Revenue, RevPAR, Occupancy %, ADR, DSRN, DBRN, DURN, and Cancellation Rate.
🛠️ Data Architecture & Star Schema
The project utilizes 5 datasets structured in a relational star schema:
Table Name
Type
Description
dim_date
Dimension
Date metadata with week numbers, months, and weekday/weekend classification.
dim_hotels
Dimension
Metadata for hotel properties (ID, name, city, category).
dim_rooms
Dimension
Room categories (RT1 to RT4) mapped to classes (Standard, Elite, Premium, Presidential).
fact_aggregated_bookings
Fact
Daily room capacity and successful bookings count aggregated by property.
fact_bookings
Fact
Detailed transactional log covering booking dates, channels, statuses, revenues, and ratings.

🧮 Key DAX Formulas & Calculated Metrics
Occupancy %: DIVIDE([Total Successful Bookings], [Total Capacity], 0)
RevPAR (Revenue Per Available Room): DIVIDE([Total Realized Revenue], [Total Capacity], 0)
ADR (Average Daily Rate): DIVIDE([Total Realized Revenue], [Total Successful Bookings], 0)
Realization %: DIVIDE([Total Realized Bookings], [Total Bookings], 0)
Cancellation Rate %: DIVIDE([Total Cancelled Bookings], [Total Bookings], 0)
🚀 How to Run the Project
Clone or download this repository:
git clone https://github.com/your-username/hospitality-revenue-analytics.git


Open Microsoft Power BI Desktop.
Open the .pbix file included in the repository.
Ensure data source file paths point correctly to the provided CSV files in the data/ directory.
🎯 Business Value
Pricing Optimization: Helps hotel management dynamically adjust rates based on weekday/weekend occupancy variations.
Leakage Reduction: Identifies direct vs. third-party channel margins and minimizes lost revenue from cancellations.
Performance Benchmarking: Enables property managers to compare underperforming locations against top-tier properties in real time.
