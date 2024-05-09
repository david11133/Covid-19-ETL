# COVID-19 Infection ETL Project

## Project Overview
This project aims to explore and analyze COVID-19 infection data sourced from John Hopkins University. The primary objective is to gain insights into the progression of the pandemic by extracting CSV data and migrating it into a PostgreSQL database.

## Project Description
The data utilized in this project was obtained from data.humdata.org and compiled by John Hopkins University. Specifically, the data was filtered for the month of March 2020 to analyze the number of confirmed cases, deaths, and recoveries.

## Data Source
All data used in this project originates from [John Hopkins University Center for Systems Science and Engineering (JHU CSSE)](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases), aggregated from reputable sources including the World Health Organization, Hong Kong Department of Health, European Centre for Disease Prevention and Control, among others.

## Data Cleanup and Analysis
### Transformation Steps
To ensure data quality and ease of analysis, the following transformation steps were undertaken:
- Developed a Python cleaning function to filter data for March 2020 across all datasets.
- Utilized the pd.melt function in Pandas to treat dates as values.
- Calculated daily increases for each metric and converted values to integers.

### Loading Steps
Data was loaded into a local PostgreSQL server for storage and subsequent analysis:
- Established a connection to a local PostgreSQL server.
- Created a schema to define tables and confirmed creation through engine.table_names().
- Transferred Pandas DataFrame to the PostgreSQL server for seamless querying.

## Analysis / SQL Queries
In the analysis phase, the following SQL queries were executed to derive insights:
- Top 5 countries with the most/least confirmed cases.
- Top 5 countries with the most/least deaths.
- Top 5 countries with the most/least recoveries.
- Date in March with the most confirmed/deaths/recoveries.

