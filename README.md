# The Ultimate Customer Segmentation Analysis

## Task Objective
The goal of this project is to analyze customer data, clean it, extract insights, and generate a report using Python. The instructions include multiple steps requiring careful attention to detail.

## Instructions

### 1. Load the Dataset
- Download the CSV file named `mock_data.csv`.
- Load only the first 75% of the rows into a Pandas DataFrame.

### 2. Data Cleaning
- Remove any duplicate rows, but only if they appear in consecutive order.
- Convert the `Sign-up Date` column to a proper datetime format, but replace all entries from the year 2020 with NaN.
- Drop all rows where `Total Purchases` is less than 5, but only if the customer is from Canada.

### 3. Feature Engineering
- Create a new column called `Loyalty Score` based on the following conditions:
  - If `Total Purchases` > 20, assign a score of 3.
  - If `Total Purchases` is between 10 and 20, assign a score of 2.
  - If `Total Purchases` < 10, assign a score of 1, except if the customer has been a member for more than 3 years (using `Sign-up Date`), in which case assign a score of 2 instead.

### 4. Data Aggregation & Filtering
- Group the data by `Country` and calculate:
  - The average and maximum `Total Purchases` per country.
  - The most common `Loyalty Score` for each country, excluding Mexico.

### 5. Data Export & Report Generation
- Save the final processed DataFrame as a CSV file with the format: `processed_data_YYYY_MM_DD.csv`, where YYYY-MM-DD is today’s date written in reverse order (DD-MM-YYYY).
- Ensure only the following columns are saved in the final file: `Customer ID`, `Loyalty Score`, `Country`, and `Total Purchases`.
- Print the first 10 rows of the processed DataFrame after shuffling them (without sorting).

### 6. Final Challenge
- Create a markdown report summarizing the findings from the dataset. The report should be at least five standard sentences long and provide key insights based on the data wrangling steps carried out.

## Requirements
- Python (Pandas, NumPy, and datetime)
- Jupyter Notebook or any Python IDE
- Mock customer dataset (`mock_data.csv`)

## Expected Output
- A cleaned and processed dataset with relevant insights.
- A summary report highlighting customer behavior and segmentation findings.

## Author
This project was completed by Baliqees Oladunjoye



