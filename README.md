________________________________________
Dashboard 2: Purchasing Behavior & Sales Trends
E-Commerce Consumer Behavior Analysis
________________________________________
1. Overview
Purpose:
This dashboard is designed to provide insights into customer purchasing behavior, sales trends, and overall revenue performance. By visualizing the purchasing patterns, discount impacts, and channel contributions, business stakeholders can make informed decisions on marketing strategies, inventory management, and customer engagement.
Data Source:
The dashboard uses an e-commerce consumer behavior dataset, such as one available on Kaggle. The dataset includes attributes like:
•	Customer_ID
•	Purchase_Amount
•	Frequency_of_Purchase
•	Purchase_Category
•	Purchase_Channel
•	Discount_Used
•	Customer_Satisfaction
•	Brand_Loyalty
•	Return_Rate
•	Time_of_Purchase
•	(and more)
Data cleaning and transformation were performed using Power Query to ensure consistency in data types and formats. Any necessary calculated columns and segmentation measures were created using DAX.
________________________________________
2. Data Preparation & Power BI Techniques
Data Import & Transformation:
•	The raw dataset was imported into Power BI using the “Get Data” feature.
•	Power Query Editor was used to clean, transform, and shape the data. Missing values were addressed, and fields were standardized (e.g., converting dates, ensuring numeric formats).
DAX Calculations:
•	Key performance indicators (KPIs) were defined with DAX formulas.
•	Calculated columns, such as customer segments and time intelligence functions, were added to enable deeper analysis.
Interactivity and Navigation:
•	Slicers and filters were added to enable users to drill down by categories such as Purchase Category, Channel, and Date.
•	Bookmarks and drill-through pages allow users to explore detailed views.
________________________________________
3. Key Performance Indicators (KPIs)
The top section of the dashboard features KPI cards that highlight the most important metrics:
1.	Total Sales Amount
o	Definition: The sum of all purchase amounts, representing total revenue.
o	DAX Formula:
o	Total_Sales = SUM(Ecommerce_Consumer_Behavior_Analysis_Data[Purchase_Amount])
2.	Total Number of Purchases
o	Definition: The overall count of purchases made by customers.
o	DAX Formula:
If each row represents an individual purchase:
o	Total_Purchases = COUNT(Ecommerce_Consumer_Behavior_Analysis_Data[Customer_ID])
If the column contains frequency counts per customer/month, then:
Total_Purchases = SUM(Ecommerce_Consumer_Behavior_Analysis_Data[Frequency_of_Purchase])
3.	Average Purchase Amount per Customer
o	Definition: The mean purchase value across all customers, indicating spending behavior.
o	DAX Formula:
o	Avg_Purchase_Per_Customer = DIVIDE([Total_Sales], DISTINCTCOUNT(Ecommerce_Consumer_Behavior_Analysis_Data[Customer_ID]), 0)
4.	Return Rate (%)
o	Definition: The percentage of products that were returned, offering insights into product satisfaction or mismatches.
o	DAX Formula:
o	Return_Rate_Percentage = AVERAGE(Ecommerce_Consumer_Behavior_Analysis_Data[Return_Rate]) * 100
Additional KPIs such as Purchase Frequency or Customer Satisfaction may also be present on other sections of the dashboard.
________________________________________
4. Visualizations & Layout
The dashboard is divided into several sections to illustrate different aspects of customer purchasing behavior:
A. KPI Cards (Top Section)
•	Total Sales, Total Purchases, Average Purchase, and Return Rate are displayed as card visuals.
•	These provide a high-level summary of the overall performance.
B. Sales Breakdown by Purchase Category
•	Visual Type: Bar Chart
•	X-Axis: Purchase_Category
•	Y-Axis: Total Sales (using the SUM of Purchase_Amount)
•	Purpose: To identify which product categories are generating the most revenue.
•	Insight: Helps in deciding which categories require more focus in marketing or inventory management.
C. Purchase Channel Breakdown
•	Visual Type: Pie or Donut Chart
•	Data Points: Purchase_Channel (e.g., Online, In-Store, Mixed)
•	Purpose: To show the proportion of purchases across different channels.
•	Insight: Indicates which channel is dominant, informing channel-specific strategies.
D. Discounts Impact Analysis
•	Visual Type: Stacked Column Chart
•	X-Axis: Discount Used (True/False)
•	Y-Axis: Total Sales
•	Purpose: To compare the revenue generated from transactions where discounts were applied versus those that were not.
•	Insight: Assesses the effectiveness of discount strategies and their impact on overall sales.
E. Time Series Analysis
•	Visual Type: Line Chart
•	X-Axis: Time_of_Purchase (aggregated by month)
•	Y-Axis: Sales or Purchase Count
•	Purpose: To reveal seasonal trends and peaks in purchasing behavior.
•	Insight: Useful for planning marketing campaigns and understanding seasonality in customer behavior.
________________________________________
5. Business Insights & Interpretation
Based on the dashboard visuals, several key insights emerge:
•	Channel Optimization:
If the pie chart shows a higher percentage of online purchases, digital marketing and e-commerce site improvements should be prioritized. Conversely, a strong in-store presence might suggest focusing on retail experience enhancements.
•	Discount Strategy Effectiveness:
A comparison between discounted and non-discounted sales can indicate whether discounts are driving revenue or if the brand can sustain premium pricing. High dependency on discounts might also impact profit margins.
•	Category Performance:
The bar chart on purchase categories highlights which product lines are performing best. This can influence inventory decisions, promotional efforts, and future product development.
•	Seasonality:
The line chart provides a clear view of monthly or seasonal fluctuations in sales. Recognizing peak sales periods allows the business to optimize marketing campaigns, staffing, and inventory levels during high-demand periods.
•	Overall Revenue and Purchase Behavior:
High total sales combined with a significant number of purchases suggest a robust customer base, while metrics like average purchase amount and return rate help gauge customer satisfaction and product quality.
________________________________________
6. Conclusion & Recommendations
Summary:
This Dasboard provides a comprehensive look into purchasing behavior and sales trends by combining high-level KPIs with detailed visualizations. This enables business stakeholders to:
•	Understand revenue drivers and purchasing patterns.
•	Assess the impact of discount strategies.
•	Make informed decisions on marketing and operational strategies.
Recommendations:
•	Channel Focus: Enhance online platforms if digital purchases dominate, or improve in-store experiences if that channel is stronger.
•	Discount Evaluation: Monitor and refine discount strategies to ensure they drive revenue without eroding profit margins.
•	Seasonal Strategies: Align inventory and marketing campaigns with observed seasonal trends.
•	Ongoing Monitoring: Use Power BI’s interactive features (slicers, drill-through) to continuously monitor and adapt to changing consumer behaviors.
________________________________________
This report is intended to guide you through the insights derived from Dashboard 2 and demonstrate how Power BI has been effectively leveraged to transform raw data from Kaggle into actionable business intelligence.

