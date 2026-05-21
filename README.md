# Telecom Customer Churn Analysis

**Author:** Adithya Machavaram    
**Tools:** SQL · Python · Power BI  
**Dataset:** IBM Telco Customer Churn (7,043 records)

## Problem Statement

A telecom company is experiencing customer churn at 26.5% monthly, resulting in ₹1.39 lakhs of recurring revenue at risk — representing 30.5% of total monthly revenue. The business lacks clarity on which customer segments drive this churn and what specific actions would reduce revenue loss. This project aims to identify churn drivers, quantify financial impact, and deliver data-backed retention recommendations.

## Executive Summary

This project analyzed 7,043 customer records to identify the root causes of customer churn. The analysis revealed three critical findings. First, month-to-month contracts churn at 42.7% — fifteen times higher than two-year contracts which churn at only 2.8%. Second, customers paying via electronic check churn at 45.3%, nearly three times the rate of auto-pay users who churn at approximately 15.2%. Third, nearly half of all churn (47.4%) occurs within the first twelve months of customer tenure.

Based on these findings, I built an interactive Power BI dashboard featuring executive KPIs, customer segmentation, revenue impact analysis, and a what-if churn reduction simulator. The dashboard also includes four actionable recommendations ranked by priority and expected revenue impact. A 10% reduction in churn would save approximately ₹1.67 lakhs annually. Implementing all four recommendations could save ₹25 to 30 lakhs per year.

---

## Process Overview

**Data Extraction.** I used SQL to extract customer data segmented by contract type, tenure, payment method, and service usage. The dataset contained 7,043 records with 21 features including monthly charges, total charges, and churn status.

**Data Cleaning.** Python with the Pandas library was used to handle missing values, particularly in the TotalCharges column where 11 records contained whitespace instead of null values. I also converted binary categorical variables to consistent formats for analysis.

**Analysis.** I wrote five SQL queries answering specific business questions about churn by contract type, tenure bucket, payment method, internet service status, and service adoption patterns. I also built a logistic regression model using scikit-learn to identify the strongest predictors of churn, which confirmed that contract type, monthly charges, and tenure are the top three drivers.

**Visualization.** All insights were compiled into a four-page Power BI dashboard with a consistent dark theme. The dashboard includes KPI cards, bar charts, line charts, donut charts, a what-if parameter for churn reduction simulation, and recommendation cards.

**Deployment.** The complete project — including code, SQL queries, dashboard file, screenshots, and this case study — is hosted on GitHub for review.

## Key Insights

**Contract Type is the Strongest Churn Driver.** Customers on month-to-month contracts churn at 42.71%, compared to 11.27% for one-year contracts and just 2.83% for two-year contracts. This represents a fifteen-fold difference between the highest and lowest risk groups.

**Payment Method Matters Significantly.** Electronic check users churn at 45.29%, while auto-pay methods perform far better. Bank transfer (automatic) users churn at 16.71%, and credit card (automatic) users churn at 15.24%. The gap between electronic check and auto-pay is nearly thirty percentage points.

**The First Year is Critical.** Customers in their first year churn at 47.44%. This drops to 28.71% in the second year, 20.39% in years two to four, and just 9.51% after four years. Retaining customers past the twelve-month mark reduces churn risk by approximately eighty percent.

**Additional Demographics.** Senior citizens churn at 41.7% — nearly double the rate of non-seniors. Fiber optic internet users churn at 41.9%, more than twice the rate of DSL users. Customers without online security churn at 41.8% compared to 14.7% for those with the add-on. Customers without a partner churn at 33.1% versus 19.7% for those with a partner. Paperless billing users churn at 33.6% compared to 16.3% for paper bill users.

## Recommendations

Based on the analysis, I have developed four recommendations ranked by expected revenue impact and implementation effort.

**High Priority — Convert Month-to-Month Customers to Annual Contracts.** Fifty-five percent of all customers (3,875 out of 7,043) are on month-to-month contracts. These customers churn at 42.7% compared to just 2.8% for two-year contract holders. Offering a 10 to 15 percent discount on annual plans could shift a meaningful portion of this segment to lower-risk contracts. Expected impact: Reduce churn from 42.7% to below 11.3%, recovering approximately ₹80,000 or more in monthly revenue.

**Medium Priority — Incentivize Auto-Pay Over Electronic Check.** Electronic check users churn at 45.3%, while auto-pay users churn at approximately 15.2%. A ₹50 monthly discount or small loyalty credit for auto-pay enrollment could shift behavior. Even converting 8 to 10 percent of electronic check users to auto-pay would yield meaningful churn reduction. Expected impact: Reduce electronic check churn by up to fifty percent, recovering approximately ₹30,000 in monthly revenue.

**Quick Win — Launch First-Year Retention Programme.** Nearly half of all churn (47.4%) happens in the first twelve months. An automated engagement sequence at months three, six, and nine — combined with a loyalty credit at month six — could keep new customers engaged through the critical first year. Expected impact: Reduce first-year churn by 15 to 20 percent, recovering approximately ₹20,000 in monthly revenue.

**Medium Priority — Upsell Online Security to Fiber Customers.** Fiber optic internet users churn at 41.9%, but customers with online security churn at only 14.7%. Bundling online security at a discounted rate for fiber customers increases switching costs and reduces churn in the highest-risk internet segment. Expected impact: Reduce fiber churn by up to fifty percent, recovering approximately ₹25,000 in monthly revenue.

**Estimated Total Impact.** If all four recommendations are implemented, the estimated annual savings range from ₹25 to 30 lakhs based on a conservative 15 percent overall churn reduction.

## Dashboard Preview

### Page 1: Executive Summary
<img width="979" height="560" alt="Page 1" src="https://github.com/user-attachments/assets/723c3e8d-48c8-4200-b905-0456e76224db" />

### Page 2: Customer Segments
<img width="977" height="557" alt="Page 2" src="https://github.com/user-attachments/assets/961b01e3-3b67-43c4-bb29-fed538238d64" />

### Page 3: Revenue Impact
<img width="972" height="559" alt="Page 3" src="https://github.com/user-attachments/assets/c8196dc8-d823-44a0-8da5-3f4b495298f4" />

### Page 4: Recommendations
<img width="975" height="556" alt="Page 4" src="https://github.com/user-attachments/assets/07b45aae-73d5-4428-a4bb-a02e39cb062e" />
