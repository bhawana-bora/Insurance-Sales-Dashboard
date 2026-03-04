📊 Sales Performance & Distribution Analytics Dashboard
Power BI Project – Life Insurance Domain
📌 Project Overview

This Power BI dashboard was developed to provide comprehensive visibility into sales performance and distribution effectiveness within a life insurance business context similar to Canara HSBC Life Insurance.

The objective of this project was to simulate a real-world Business Analyst engagement — starting from requirement analysis and BRD preparation to data modeling, DAX development, dashboard design, and UAT validation.

This solution focuses primarily on:

Regional sales monitoring

Branch and agent-level performance analysis

Channel contribution analysis

KPI trend tracking using time intelligence

🎯 Business Objective

The dashboard aims to:

Monitor Gross Written Premium (GWP) growth

Track policy sales performance across regions

Identify top and underperforming agents

Analyze distribution channel contribution

Enable management-level drill-down insights

🏗️ Data Model Architecture

The report follows a Star Schema Data Model for optimized performance and scalability.


![Data Model](https://github.com/user-attachments/assets/6d7e5088-17b5-41fe-8c5f-5131748e024f)





🔹 Fact Table
Fact_Sales

Contains transactional-level policy sales data:

Policy_ID

Customer_ID

Agent_ID

Branch_ID

Product_ID

Policy_Date

Premium_Amount

APE

Payment_Mode

Policy_Status

🔹 Dimension Tables
Dim_Customer

Customer_ID

Age

Gender

City

Income_Bracket

Dim_Agent

Agent_ID

Agent_Name

Experience_Years

Channel (Bancassurance / Direct / Online)

Branch_ID

Dim_Branch

Branch_ID

Branch_Name

Region

State

Dim_Product

Product_ID

Product_Name

Product_Type

Risk_Category

Dim_Date

Custom date table created using DAX to support:

Year

Month

Quarter

Year-Month

Time intelligence calculations

📈 Dashboard Structure
🔹 Page 1 – Executive Summary

![Executive summary](https://github.com/user-attachments/assets/4514988c-97e2-43ef-b010-674c7dbe993a)


This page provides a high-level overview for senior leadership.

Includes:

Total Premium

Total Policies

Total APE

Lapse Rate

Monthly Premium Trend

Region-wise contribution

Channel distribution (Donut Chart)

Purpose:
Enable quick health check of overall business performance.

🔹 Page 2 – Sales Performance

![Sales performance](https://github.com/user-attachments/assets/9709b0c2-93f4-4a5e-b110-da96dd096d56)


This page focuses on diagnostic analysis.

Includes:

1. Premium by Region (Bar Chart)

Displays premium distribution across regions to identify high and low performing geographies.

2. Region → Branch → Agent Matrix

Interactive drill-down matrix allowing:

Region-level overview

Branch-level performance comparison

Agent-level granular analysis

3. Top 10 Agents (Dynamic Ranking)

Implemented using DAX RANKX function to:

Rank agents by Total Premium

Dynamically filter Top 10 performers

Identify revenue concentration risk

Purpose:
Identify distribution efficiency and channel growth opportunities.

📊 Key DAX Measures Implemented

Total Premium

Total Policies

Total APE

Premium YTD

MoM Growth %

Lapsed Policies

Lapse Rate

Agent Rank (RANKX-based dynamic ranking)

Channel Contribution %

🔎 Analytical Features

Drill-down functionality (Region → Branch → Agent)

Time intelligence (YTD, MoM)

Dynamic ranking

Contribution analysis

Conditional formatting for performance highlighting

🧪 UAT & Validation Approach

As part of the Business Analyst simulation:

Sample policy records were manually reconciled with source data

APE calculations were validated across payment modes

Lapse Rate formula verified against filtered scenarios

Drill-down totals tested for aggregation accuracy

This ensured business logic consistency before finalization.

⚙️ Tools & Technologies Used

Power BI Desktop

DAX (Data Analysis Expressions)

Excel (Mock Data Generation)

Star Schema Data Modeling

🚀 Future Enhancements (Not Implemented)

Claims Ratio Dashboard

NPS (Net Promoter Score) Analysis Page

Role-Level Security (RLS) by Region

Target vs Achievement KPI page

Persistency Ratio (13th / 25th month cohort analysis)

👨‍💼 My Role in the Project

Requirement gathering simulation

BRD preparation

Data model design (Star Schema)

DAX development

Dashboard design & layout

UAT scenario validation
