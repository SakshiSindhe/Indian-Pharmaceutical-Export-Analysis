Code Explanation

This Python code analyses India's pharmaceutical exports under HS Code 30 using monthly country-wise export data from the Government of India, DGCIS / TRADESTAT.

1. Data Loading and Inspection

The code imports the required Python libraries and loads the CSV dataset. It checks the first few records, data structure, data types and descriptive statistics to understand the dataset before analysis.

2. Data Cleaning and Restructuring

The monthly export columns are identified and the existing TOTAL row is removed to avoid double-counting. The dataset is then converted from wide format into long format with four main fields: Country, Financial Year, Month and Export Value.

Incomplete financial-year data is removed, export values are converted into numeric form, and missing and duplicate observations are checked before further analysis.

3. Date and Financial-Year Preparation

The code creates month numbers, calendar months, financial-year starting years and proper date values. This is important because India's financial year runs from April to March. The data is then arranged chronologically for time-based analysis.

4. Monthly and Financial-Year Analysis

Monthly total pharmaceutical exports are calculated by adding exports across all countries. The code also calculates previous-month exports and month-on-month growth. Monthly values are then grouped into financial years to compare annual export performance and growth.

5. Country-Wise Market Analysis

The code calculates total exports for each country across financial years. For FY 2025-26, it calculates export value, growth percentage, market share and coefficient of variation (CV).

These measures help compare international markets based on their size, recent growth and stability.

6. Descriptive Analysis and Visualisation

The code generates different charts to understand export patterns. These include monthly export trends, financial-year comparisons, the top 10 export markets, the combined share of the top 10 markets, the distribution of export values across countries and monthly variation in major markets.

7. Predictive Analysis

A simple linear regression model is used to examine whether the previous month's pharmaceutical exports can be used to estimate the current month's exports.

The data is divided into 80% training data and 20% testing data. The model learns the relationship between previous-month and current-month exports and then generates predictions for the test data.

8. Model Evaluation

The predictions are evaluated using MAE, RMSE and R-squared (R²).

MAE measures the average prediction error, RMSE gives more importance to larger prediction errors, and R² indicates how well previous-month exports explain the variation in current-month exports.

The actual and predicted values are also presented in a table and compared using a line chart.

9. Output Files

The code saves the cleaned dataset, financial-year summary, country-wise market summary and regression predictions as separate CSV files for further use and reference.

### Overall Purpose

The code combines descriptive and predictive analysis to understand India's pharmaceutical export performance, identify important international markets based on export value, growth and stability, and examine whether previous-month export performance can be used to estimate current-month exports.
