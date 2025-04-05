# Performance-Data-Visualization-Dashboard

## Overview

This dashboard provides a comprehensive view of key performance indicators (KPIs) to track progress against targets. It allows users to monitor actual performance, compare it to targets, understand trends over time, and analyze the contributions of different teams and individuals.

## Data Sources

The dashboard utilizes data from the following tables:

* **Actual (Fact Table):** Contains the actual performance data, such as sales figures, for specific periods and individuals/teams.
* **Target (Fact Table):** Contains the target performance data, corresponding to the actual data in the "Actual" table.
* **Calendar (Dimensional Table):** Provides a date dimension, enabling time-based analysis.
* **DimPeople (Dimensional Table):** Contains information about individuals or teams, allowing for performance breakdown by these dimensions.

## Data Preparation

The following steps were undertaken to prepare the data for this dashboard:

1.  **Data Upload:** Four distinct tables ("Actual," "Target," "Calendar," and "DimPeople") were uploaded to the data model.
   
2.  **Data Cleaning:**:
    * Handling missing values (e.g., imputation, removal).
    * Correcting data inconsistencies (e.g., standardizing naming conventions).
    * Removing duplicate records.
    * Ensuring data type consistency across related fields.
      
3.  **Data Feature Engineering:**
    * From the "Calendar" table, the following features were extracted to facilitate time-based analysis:
        * Year
        * Month (numeric representation)
        * Month Name (e.g., January, February)
          
4.  **Data Modeling:**
    * The "Calendar" table was joined to both the "Actual" and "Target" tables using relevant date fields.
    * Relationships were established between all tables ("Actual," "Target," "Calendar," and "DimPeople") to ensure data integrity and enable seamless analysis across dimensions. The data model was designed with appropriate cardinalities and filter directions.

## DAX Calculations

The dashboard leverages the following Data Analysis Expressions (DAX) to derive key performance metrics:

* **Total Sales Actual:** Calculates the sum of actual sales from the "Actual" table.
* **Total Sales Target:** Calculates the sum of target sales from the "Target" table.
* **Variance:** Calculates the difference between "Total Sales Actual" and "Total Sales Target."
* **Variance %:** Calculates the percentage difference between actual and target sales, relative to the target.
* **YTD Sales Actual:** Calculates the year-to-date (YTD) sum of actual sales.
* **Target Status:** Determines whether the actual sales have met, exceeded, or fallen below the target.
* **Previous Year Sales:** Calculates the sales for the corresponding period in the previous year.
* **Month Target Reached:** Indicates whether the monthly sales target has been achieved.

## Dashboard Preparation and Visualizations

The dashboard is structured to provide an intuitive and insightful view of performance:

* **New Card Visuals:** Used to display key aggregate measures prominently, such as "Total Sales Actual," "Total Sales Target," "Variance," and "Variance %."
* **Clustered Bar Chart:** Visualizes month-to-month performance, allowing for easy comparison of actual sales against targets and identification of trends over time.
* **Table Visual:** Provides a summarized view of sales performance broken down by salesperson, displaying key metrics and enabling detailed individual performance analysis.
* **Slicer for Team Display:** Allows users to filter the dashboard to focus on the performance of specific teams, facilitating comparative analysis between different groups.

## How to Use the Dashboard

* **Overview:** The top section with the new card visuals provides a high-level snapshot of overall performance against targets.
* **Trend Analysis:** Use the clustered bar chart to observe monthly performance trends and identify seasonal patterns or significant changes over time.
* **Individual Performance:** The table visual allows you to assess the performance of individual salespeople based on various metrics.
* **Team Comparison:** Utilize the "Team" slicer to filter the data and compare the performance of different teams.

## Contact

For any questions or issues related to this dashboard, please contact ogechifaith78@gmail.com.

Follow me on linkedin : https://www.linkedin.com/in/ogechifaith
