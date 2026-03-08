# Covid_19
COVID-19 Time Series Data Analysis
Project Overview

This project analyzes global COVID-19 data using Python and pandas. The goal of the project is to clean, combine, and analyze pandemic datasets to understand trends in confirmed cases, deaths, and recoveries. The analysis also identifies peak infection surges and compares recovery performance across countries.

The project uses three datasets containing global COVID-19 statistics:

Confirmed cases

Death cases

Recovered cases

These datasets were processed and transformed into a unified time-series dataset for analysis.

Dataset Description

The project uses three datasets:

Confirmed Cases Dataset – Contains cumulative confirmed COVID-19 cases for countries and provinces over time.

Deaths Dataset – Contains cumulative death counts due to COVID-19.

Recovered Dataset – Contains cumulative recovered case counts.

Important columns in the datasets:

Province/State – Sub-region within a country

Country/Region – Country name

Lat / Long – Geographic coordinates

Date columns – Daily cumulative counts

Data Processing Steps
1. Load the Datasets

The datasets were loaded using pandas for analysis.

import pandas as pd
2. Explore the Dataset

Initial exploration was performed using:

head()

info()

shape()

This helped understand dataset structure, column types, and missing values.

3. Reshape the Dataset

The datasets originally stored dates as columns (wide format).
They were converted into long format using pandas.melt() to enable time-series analysis.

Resulting structure:

| Province | Country | Date | Confirmed |

4. Merge the Datasets

The confirmed, deaths, and recovered datasets were merged into a single dataset using common columns:

Province/State

Country/Region

Date

The final dataset contains:

Confirmed

Deaths

Recovered

5. Handle Missing Values

Several missing values were identified after merging.

The following steps were applied:

Missing values in Province/State were replaced with "All Provinces"

The dataset was sorted by country, province, and date

Forward filling (ffill) was applied for cumulative time-series values

Forward fill is suitable because COVID-19 case counts are cumulative.

Analysis Performed
1. Global Trend Analysis

Time-series plots were generated to visualize confirmed cases for top countries. This helps understand pandemic waves and growth patterns.

2. China Trend Analysis

A similar trend plot was created for China to observe the progression of the outbreak in the earliest affected region.

3. Peak Daily New Cases Analysis

Daily new cases were calculated using the difference between consecutive days:

Daily_New_Cases = Confirmed.diff()

Countries analyzed:

Germany

France

Italy

Result:

France recorded the highest single-day surge on April 11, 2021, with 117,900 new cases.

4. Recovery Rate Comparison

Recovery rate was calculated using:

Recovery Rate = Recovered / Confirmed

Countries compared:

Canada

Australia

Results:

Australia had a recovery rate of 79.38%.

Canada showed 0% recovery rate in the dataset due to missing recovery data reporting.

Key Insights

France experienced the highest daily surge among Germany, France, and Italy.

Australia showed a strong recovery rate relative to confirmed cases.

Data quality issues such as missing recovery data can affect analytical conclusions.

Technologies Used

Python

Pandas

Matplotlib

Jupyter Notebook

Project Structure
covid19-analysis
│
├── data
│   ├── confirmed_cases.csv
│   ├── deaths.csv
│   └── recovered.csv
│
├── notebooks
│   └── covid_analysis.ipynb
│
└── README.md
Learning Outcomes

Through this project the following skills were applied:

Data cleaning and preprocessing

Handling missing values

Time-series data transformation

Dataset merging

Exploratory data analysis

Trend analysis and visualization

Author

Anusha
Data Analytics Enthusiast
Python | Pandas | Data Analysis
