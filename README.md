# Customer Segmentation Using RFM Analysis – Power BI Dashboard

## Overview

This project presents a **Customer Segmentation Dashboard** created in **Power BI** using **RFM Analysis (Recency, Frequency, Monetary)** methodology. The dashboard enables businesses to analyze customer purchasing behavior, segment their customer base, and apply tailored marketing strategies to improve engagement, retention, and revenue.

---

## What is RFM Analysis?

**RFM Analysis** segments customers based on their transaction history:

- **Recency (R):** How recently a customer made a purchase.
- **Frequency (F):** How often a customer makes a purchase.
- **Monetary (M):** How much money a customer spends.

These three metrics are scored and combined into a unique **RFM Score** (e.g., 511, 344) which is then mapped to customer segments such as **Champions**, **Loyal**, **At Risk**, etc.

---

## Objectives

- Understand customer demographics and sales distribution.
- Segment customers using RFM methodology.
- Identify high-value vs. low-engagement customers.
- Recommend marketing actions based on customer segments.

---

## Dataset Details

Data is sourced from a fictional sales dataset resembling **AdventureWorks**. The key tables used:

- `FactInternetSales`: Transactional sales data.
- `DimCustomer`: Customer profiles (age, gender, location).
- `DimDate`, `DimGeography`, `DimProduct`: Supporting dimensional tables.
- `RFM Table`: Custom table containing RFM scores and segments.

---

## Data Model

The data model includes well-defined relationships between dimensions and fact tables. Here's a summary:

- **1-to-many relationships** from dimension tables (e.g., `DimCustomer`, `DimDate`) to `FactInternetSales`.
- **Custom RFM scoring logic** calculated using DAX.
- **Segment mapping** handled via lookup tables (`Segment Table`, `Segment Descriptions`).
  ![image](https://github.com/user-attachments/assets/ccbc1b7e-ba5b-43c6-a671-0ab5d4d88786)




# RFM Dashboard – Report Analysis & Recommendations

This report provides a structured analysis of each page in the RFM-based Power BI dashboard. It highlights key metrics, interprets user behavior patterns, and offers actionable business recommendations.

---


## Page 1: Customer Demographics

![image](https://github.com/user-attachments/assets/50b3c3e3-cd3e-4716-ae49-2e612feb7cda)

### Key Metrics
- **Total Sales**: $29.36 million  
- **Number of Customers**: 18,484  
- **Gender Distribution**: Male (50.46%), Female (49.54%)  
- **Marital Status**: Married (51.73%), Single (48.27%)  


### Sales by Age Band
- 55–64: $11.4M  
- 65–74: $7.7M  
- 45–54: $6.4M  


### Geographic Breakdown
Strongest sales are concentrated in North America, Europe, and Australia.


### Analysis
The data suggests that the majority of revenue is driven by older customer groups, particularly those between 55 and 74 years old. Gender and marital status distributions are well-balanced, indicating broad customer appeal without apparent bias. Regionally, sales are largely generated from mature markets in the Western hemisphere.


### Recommendations
- Focus marketing and retention strategies on the 55–74 age group, as they represent the most valuable customer demographic.
- Invest in campaigns targeted at North America and Europe to maximize regional performance.
- Ensure the customer experience (especially digital interfaces) is optimized for older users with accessible design and clear communication.

---


## Page 2: Customer Segmentation (RFM Analysis)

![image](https://github.com/user-attachments/assets/d79f9925-5136-4e1f-9259-1c2fa02c8ebc)

### Segment Summary

| Segment         | Customers | Total Sales |
|----------------|-----------|-------------|
| Champions       | 1,700     | $8.3M       |
| Loyal           | 1,800     | $6.2M       |
| At Risk         | 1,800     | $7.3M       |
| Promising       | 2,600     | $2.9M       |
| New Customers   | 3,200     | $0.1M       |
| Hibernating     | 1,500     | $0.1M       |
| About to Sleep  | 1,100     | $0.3M       |
| Need Attention  | 300       | $0.0M       |


### Analysis
Over half of the total revenue comes from Champions and At Risk customers combined. While Champions are highly active and loyal, At Risk customers were once valuable but have not made recent purchases.

New Customers make up the largest segment by count but contribute minimally to revenue. This suggests an issue with early-stage customer engagement or conversion.

Promising customers show good potential and recent engagement but are not yet delivering high value.


### Recommendations
- Prioritize re-engagement campaigns for At Risk customers using personalized offers or loyalty incentives.
- Improve onboarding strategies for New Customers through first-purchase offers, welcome content, and product education.
- Nurture Promising customers with promotional campaigns aimed at increasing repeat purchases and moving them toward Loyal or Champion segments.
- Invest in retaining Champions through loyalty programs, exclusive access, and priority service.

---

## Page 3: Customer Details

![image](https://github.com/user-attachments/assets/a6ef9979-db55-4c20-97e5-fd14abc4d58a)


### Example Insight – Top Customer
- **Customer**: Hunter Lopez  
- **Recency**: 6,194 (days since last purchase)  
- **Frequency**: 1  
- **Monetary Value**: $2,564.92  
- **Segment**: Promising  


### Analysis
The top customers by sales are typically older, high-spending individuals who have only made a single purchase. This points to a missed opportunity to convert high-value, one-time buyers into repeat customers.

Additionally, these top customers are geographically dispersed, mainly across the United States, United Kingdom, Germany, and France.


### Recommendations
- Introduce cross-sell and upsell offers to increase frequency among high-Monetary, low-Frequency customers.
- Target high-value one-time buyers with follow-up emails or special incentives to encourage repeat purchases.
- Develop region-specific campaigns for strong-performing countries to enhance localization and relevance.

---

## Page 4: RFM Description and Marketing Strategy

![image](https://github.com/user-attachments/assets/5770f7ba-6e80-4e85-87d1-e76828a6fa15)


### Overview
This page outlines behavioral descriptions and recommended actions for each RFM segment. It acts as a guide for aligning marketing strategy with customer behavior.


### Segment Application
- **Champions**: Continue to reward loyalty and maintain engagement.  
- **Loyal**: Provide recognition and consistent service.  
- **At Risk**: Implement reactivation strategies and monitor behavior closely.  
- **New and Promising**: Focus on education, onboarding, and early retention.  


### Recommendations
- Automate marketing actions using CRM or email platforms to trigger campaigns when customers move between segments.
- Monitor segment transitions over time to measure the effectiveness of customer engagement strategies.
- Collaborate across teams (marketing, support, product) to implement aligned actions for each customer segment.

---

## Summary

The RFM analysis reveals strong opportunities to:

- Increase revenue by focusing on existing high-value customers.
- Reduce churn by proactively engaging At Risk and Hibernating segments.
- Improve conversion of New Customers through better onboarding and follow-up.
- Leverage demographic and geographic patterns to guide personalized marketing.

This report supports the use of RFM as a practical and effective tool for customer segmentation and strategic decision-making in customer relationship management.
For more details about the DAX code, please view the Power BI File

