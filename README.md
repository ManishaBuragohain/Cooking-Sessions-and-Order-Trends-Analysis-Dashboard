# Cooking Sessions and Order Trends Analysis Dashboard

# Table of Contents

1. Project Overview

2. Datasets Used

3. Data Cleaning and Preparation

4. Key Insights and Visualizations

5. DAX Measures

6. Conclusion and Recommendations

7. Tools Used

8. How to Use

9. Author

# Project Overview
This project focuses on analyzing datasets related to user behavior, cooking preferences, and order trends. The goal is to uncover key insights about user engagement, popular dishes, and meal types.

An interactive Power BI dashboard has been created to visually present these findings. The analysis highlights important trends in user preferences and provides actionable insights to improve efficiency and user satisfaction.

By using calculated measures and clear visualizations, this project helps in making informed decisions based on data.


# Datasets Used

The project utilizes the following datasets:

# UserDetails: 
Contains user demographic information.

# CookingSessions: 
Includes session details such as duration, meal type, and dishes cooked.

# OrderDetails: 
Tracks order information, including dish names, order amounts, and statuses.

# Data Cleaning and Preparation

Key Steps:

Data Integration: Merged the three datasets using User ID and Session ID as keys.

Data Transformation: Standardized column names and formats.

Handling Missing Values: Checked for missing data and addressed inconsistencies.

Calculated Fields:

Measures like total revenue, completed orders, and average session duration were created using DAX formulas in Power BI.

# Key Insights and Visualizations

# 1. Popular Dishes Analysis

Visualization: Stacked Bar Chart.

X-axis: Count of Order ID.

Y-axis: Order Dish Name.

Insight: Identified the most frequently ordered dishes by users.

# 2. Revenue Trend Over Time

Visualization: Line Chart.

X-axis: Order Date.

Y-axis: Total Revenue.

Insight: Displayed revenue trends across different time periods.

# 3. Session Duration by Meal Type

Visualization: Clustered Column Chart.

X-axis: Meal Type.

Y-axis: Average Session Duration (mins).

Insight: Highlighted meal types with longer or shorter preparation times.

# 4. Cancelled vs. Completed Revenue

Visualization: Tree Map.

Category: Order Status.

Values: Revenue.

Insight: Compared the revenue contribution of completed and cancelled orders.

# 5. User Distribution by Location

Visualization: Map.

Location: User Location.

Legend: Total Orders.

Insight: Showed user density across different geographic regions.

# DAX Measures

Below are some calculated measures used in Power BI:

# Total Revenue:

Total Revenue = SUM('OrderDetails'[Amount (USD)])

# Average Session Duration:

Average Session Duration = AVERAGE('CookingSessions'[Duration (mins)])

# Completed Revenue:

Completed Revenue =
CALCULATE(SUM('OrderDetails'[Amount (USD)]),
'OrderDetails'[Order Status] = "Completed")

# Percentage of Completed Orders:

Percentage of Completed Orders =
DIVIDE(CALCULATE(COUNT('OrderDetails'[Order ID]), 'OrderDetails'[Order Status] = "Completed"),
COUNT('OrderDetails'[Order ID]),
0) * 100

# Preview

![image](https://github.com/user-attachments/assets/c58ac008-9312-45a1-9216-486ccef7ffed)

![image](https://github.com/user-attachments/assets/0d6aa319-e74a-49b2-8622-dc9488db6d51)

![image](https://github.com/user-attachments/assets/410f06c8-f6e0-4833-b9a4-6e39885dac96)




# Conclusion and Recommendations

# Key Takeaways:

Popular Dishes: Focus on dishes that drive high user engagement.

Meal Type Insights: Optimize session durations for meal types with longer preparation times.

Order Status: Minimize cancellations to improve revenue.

Revenue Trends: Target marketing campaigns during low-revenue periods.

# Tools Used

Power BI: For creating interactive dashboards.

Python: For data cleaning and transformation.

Excel: For preliminary analysis.

# How to Use

Clone this repository to your local system:

git clone https://github.com/ManishaBuragohain/Cooking-Sessions-and-Order-Trends-Analysis-Dashboard.git

Open the Power BI file (Dashboard.pbix) to explore the interactive dashboard.

View the Jupyter Notebook for data cleaning and analysis steps.

# Author

# Manisha Buragohain

GitHub Profile

