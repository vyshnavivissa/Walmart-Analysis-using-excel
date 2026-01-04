## Introduction

The objective of this project was to analyze Walmart’s weekly sales data from 2010 to 2012 to identify sales trends, evaluate store-level performance, and examine how external economic and environmental factors—such as temperature, holidays, CPI, fuel prices, and unemployment—impact retail sales. This project demonstrates my ability to clean, analyze, and visualize real-world data using Microsoft Excel, culminating in an interactive dashboard with slicers and timelines for dynamic analysis.

The dataset, **Walmart_Sales**, was sourced from Kaggle and contains **6,434 rows** of weekly sales data covering **45 Walmart store locations** from **February 2010 to October 2012**.

### Dataset Columns

* **Store** – Unique store identifier
* **Date** – Week start date
* **Weekly_Sales** – Weekly sales (USD)
* **Holiday_Flag** – Indicator for holiday weeks (1 = Holiday, 0 = Non-holiday)
* **Temperature** – Average weekly temperature (°F)
* **Fuel_Price** – Average fuel price per gallon
* **CPI** – Consumer Price Index
* **Unemployment** – Unemployment rate

## Data Preparation & Cleaning

After importing the dataset into Excel, I performed an initial data quality assessment:

* Checked for **duplicate records and missing values** using filters (none were found).
* Ensured consistent and correct **data formatting** across all columns.

### Date Formatting Issue

The Date column contained two different formats (DD/MM/YY and DD-MM-YYYY), which caused Excel to inconsistently recognize values as dates.

**Steps taken:**

1. Cleared all formatting to reset the worksheet.
2. Added a helper column using `ISNUMBER()` to identify which date values were correctly interpreted by Excel.
3. Used **Text to Columns** to standardize all dates to a single **DD/MM/YY** format.

### Data Formatting Adjustments

* Converted **Weekly_Sales** and **Fuel_Price** to Accounting format.
* Reduced decimal places for **Temperature, Fuel Price, CPI, and Unemployment** for cleaner visuals.
* Converted **Unemployment** to percentage format using a helper column (value ÷ 100).

These steps ensured consistency, accuracy, and readability for downstream analysis and dashboard visuals.

## Exploratory Data Analysis (EDA)

To understand the overall structure and distribution of the data, I generated summary statistics using Excel’s **Analysis ToolPak**.

Key takeaways from EDA:

* Established baseline values for **average weekly sales, CPI, fuel prices, and unemployment**.
* Identified **seasonal sales spikes** and potential outliers using max and min values.
* Confirmed that sales variability was substantial across stores and time periods, justifying deeper segmented analysis.

## Analysis & Visualizations

Using Pivot Tables, Pivot Charts, slicers, and timelines, I created multiple interactive visualizations, all integrated into a consolidated dashboard.

### 1. Sales Time-Trend Analysis by Store

**Objective:** Compare sales trends across all 45 stores over time.

**Methodology:**

* Pivot table with weekly sales aggregated by date.
* Line chart with **store slicer** and **timeline control**.

**Insights:**

* Clear **seasonal patterns**, with consistent peaks in **December** across nearly all stores.
* Additional recurring increases observed during early **Q2 and Q3**, indicating secondary seasonal demand cycles.

### 2. Top 5 Stores by Total Sales

**Objective:** Identify the highest-performing stores across years.

**Methodology:**

* Pivot table with **Store** in rows and **Date (Year)** in columns.
* Bar chart connected to the dashboard timeline.

**Insights:**

* **Store 20** emerged as the top-performing store overall, ranking consistently high every year.
* **Store 4** showed strong, stable performance across all years.
* **Store 14** entered the Top 5 in 2010 and 2012, placing third overall despite variability.

### 3. Yearly Sales Comparison

**Objective:** Compare Walmart’s total sales by year.

**Methodology:**

* Pivot table aggregating yearly sales.
* Column chart visualization.

**Insights:**

* **2011 recorded the highest total sales** among the three years.
* 2012 sales appear lower due to **missing Q4 data**, likely understating actual annual performance.
* Given post-2008 economic recovery trends and Walmart’s value-oriented positioning, full-year 2012 data would likely show positive YoY growth.

### 4. Holiday vs Non-Holiday Sales Impact

**Objective:** Measure the effect of holidays on weekly sales.

**Methodology:**

* Pivot table grouped by **Holiday_Flag**.
* Comparison of average weekly sales.

**Insights:**

* Holiday weeks consistently generated **higher average sales**.
* Major spikes observed around **Thanksgiving and Christmas**, confirming strong holiday-driven consumer spending behavior.

### 5. Temperature vs Sales Distribution

**Objective:** Assess how weather affects sales volume.

**Methodology:**

* Scatter plot of **Weekly Sales vs Temperature**.

**Insights:**

* Highest sales occurred when temperatures were between **30°F and 50°F**.
* Extremely hot or cold temperatures were associated with lower sales, suggesting weather influences shopping activity.

### 6. Inflation (CPI) vs Month-over-Month Sales Growth

**Objective:** Evaluate the relationship between inflation and sales performance.

**Methodology:**

* Pivot table calculating MoM sales growth and CPI.
* Dual-axis line chart.

**Insights:**

* Periods of rising CPI occasionally aligned with slower sales growth.
* Overall, Walmart’s sales demonstrated **resilience to inflation**, likely due to its focus on affordable essentials.

### 7. Unemployment Rate vs Weekly Sales

**Objective:** Understand the impact of employment levels on consumer spending.

**Methodology:**

* Line chart comparing weekly sales and unemployment rates.

**Insights:**

* Higher unemployment rates generally coincided with **lower sales**.
* Confirms that consumer purchasing power is closely tied to job market conditions.

## Dashboard-Level Key Insights

1. **Holidays significantly boost sales**, especially in December.
2. **Unemployment has a strong inverse relationship with sales**, highlighting economic sensitivity.
3. **Walmart’s sales remain relatively inflation-resistant**, reinforcing its value-based business model.
4. **Moderate temperatures (30–50°F) are associated with peak sales**, indicating weather-driven shopping behavior.

## Reflections & Next Steps

This project strengthened my Excel-based data analytics skills, particularly in:

* Data cleaning and validation
* Pivot table–driven analysis
* Building interactive dashboards using slicers and timelines

### Future Enhancements

* Incorporate additional macroeconomic indicators (consumer sentiment, income levels).
* Use **SQL or Python** to scale analysis for larger datasets.
* Build **predictive models** to forecast sales using historical and economic variables.

## Conclusion

This Walmart Sales Analysis project successfully demonstrates my ability to clean, analyze, and visualize complex retail data using Excel. By examining sales trends from 2010–2012, I identified key drivers of retail performance, including holidays, unemployment, inflation resilience, and temperature effects. The insights derived from this analysis can support data-driven decision-making in retail strategy, forecasting, and operations planning. I plan to further expand this work using advanced analytics tools to generate deeper business insights.
