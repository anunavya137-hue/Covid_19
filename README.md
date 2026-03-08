# Covid_19
# COVID-19 Data Analysis Project

## Project Overview
This project analyzes COVID-19 datasets to understand the spread, recovery patterns, and overall impact across different countries/regions. The analysis involves data cleaning, merging multiple datasets, calculating recovery rates, and generating insights using Python and pandas.

## Dataset
The dataset contains the following information:
- Country/Region
- Confirmed cases
- Recovered cases
- Recovery Rate

## Steps Performed

### 1. Data Loading
Loaded multiple COVID-19 datasets using pandas.

### 2. Data Merging
Merged all datasets into a single dataframe using common columns such as Country/Region.

### 3. Data Cleaning
- Removed unnecessary columns
- Handled missing values
- Converted data types where required

### 4. Feature Engineering
Created a new column:
Recovery Rate = Recovered / Confirmed

### 5. Data Analysis
Performed analysis to identify:
- Countries with highest confirmed cases
- Countries with highest recovery rates
- Overall recovery trends

## Sample Output

| Country/Region | Confirmed | Recovered | Recovery_Rate |
|---------------|-----------|-----------|---------------|
| Australia | 28425 | 22565 | 0.79 |
| Canada | 584409 | 0 | 0.00 |

## Tools & Technologies Used
- Python
- Pandas
- Jupyter Notebook
- GitHub

## Key Insights
- Some countries have high confirmed cases but low recovery rates.
- Recovery rate helps understand healthcare response effectiveness.

## Conclusion
The project demonstrates how data analysis techniques can be used to derive meaningful insights from COVID-19 datasets.

## Author
Anusha
