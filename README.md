# Background Project
SwiftBite Delivery faces challenges in maintaining delivery speed and efficiency amidst high order volumes and dynamic traffic conditions. The average delivery time stands at 26.29 minutes.
Traffic congestion, peak hour, workload delivery and the complexity of delivery distances contribute to operational bottlenecks that result in delivery delays and reduced operational efficiency.
This project aims to develop an operational monitoring dashboard to help the operations team monitor traffic bottlenecks, operational risks, delivery performance and delivery efficiency.

# Business Problem

- Identify operational conditions that contribute to increased delivery times and delivery bottlenecks
- Monitor the distribution of operational risk based on traffic conditions, delivery workload and delivery operational patterns
- Evaluate delivery efficiency based on delivery distance and its impact on delivery performance

# Analytical Questions

- Which traffic conditions result in the longest delivery times?
- When do delivery bottlenecks occur most frequently?
- Does the delivery workload increase delivery delays?
- Which operational risk category has the longest delivery times?
- Which area has the highest proportion of High-Risk orders?
- When do High-Risk orders occur most frequently?
- Does delivery distance affect delivery times?
- Which delivery distance category has the highest operational risk?

# Data Understanding

Dataset Source: Zomato Delivery Operations Analytics

Dataset Overview: 45.584 order delivery records dan 20 operational delivery features for the year 2022

Category Features: 
- Traffic & operational environment
- Operational delivery
- Geolocation
- Time-based features

Data Quality Issues:
- Missing values in operational features
- Inconsistent time data formats
- Invalid coordinate data
- Anomalies in delivery distances

Operational Traffic ipynb: https://colab.research.google.com/drive/1l0wYaYomI8yJRKDRwwljY2EUCDQIiTrL?usp=sharing

# Operational Risk Scoring

Identify several operational factors, namely traffic density, multiple deliveries, peak-hour conditions, delivery distance, pickup delay duration, and weather conditions.
Next, each feature is assigned a score of 1–3 based on the extent of its impact on operational delivery constraints; the scores for each row are then totaled to give a total score, which is categorized into operational risk categories such as Low Risk, Medium Risk and High Risk, with the risk score range defined by the minimum, median and maximum values.

# Analysis
Traffic Bottleneck Analysis

<img width="1123" height="239" alt="image" src="https://github.com/user-attachments/assets/694c3731-9e38-4542-8d1e-d71afdfd7074" />

Insight:
- Peak traffic times result in the longest delivery times, and delivery times increase as traffic density rises
- Delivery bottlenecks occur most frequently during the dinner period
- Multiple deliveries increase delivery times and exacerbate operational bottlenecks

High-Risk Delivery

<img width="1199" height="267" alt="image" src="https://github.com/user-attachments/assets/f8fdd8e7-0c05-4c89-a65c-4ff452e54f38" />

Insight:
- High-risk orders have the longest average delivery time
- High-risk operational issues occur most frequently during the dinner peak period **~54%**
- Semi-Urban areas account for the largest proportion of high-risk orders **~72%**

Delivery Distance & Operational Risk

<img width="1309" height="348" alt="image" src="https://github.com/user-attachments/assets/2e19511a-2dfa-4f3b-97b3-24d17b57fe65" />

Insight:
- Long-distance deliveries have the highest average delivery time
- Operational risk increase as delivery distance increases, with long-distance operations accounting for the highest proportion of high-risk deliveries **~40%**

# Recommendation

- Optimizing workload allocation to reduce operational overload
- Prioritizing operational monitoring in semi-urban areas to reduce the concentration of high-risk deliveries
- Implementing route optimization for long-distance deliveries to improve delivery efficiency
