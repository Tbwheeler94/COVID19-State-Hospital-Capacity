# COVID19-State-Hospital-Capacity

## Extract
### We used 2 datasets from the [Uncover COVID19 Challenge](https://www.kaggle.com/roche-data-science-coalition/uncover/version/3) on Kaggle. 

Dataset 1: Covid-statistics-by-us-states-totals.csv which includes (by U.S. state): 

  1. Positive and negative test results
  2. Total test results  

Dataset 2: Hospital-capacity-by-state-20-population.csv which includes (by U.S. state): 

  1. Available hospital beds
  2. Available icu beds
  3. The projected number of potentially infected individuals
  4. The projected number of those individuals needing hospitalization
  5. Total hospital beds
  6. Total icu beds
  7. Adult population

## Transform
### We used the following transformations to clean and prepare our data for loading

1. Dropped unnecessary columns
2. Changed index to state
3. Joined two tables of data by state
4. Calculated rate of infected people needing hospitalization (assumed 7% based on [Massachusetts Department of Public Health COVID-19 Dashboard data](https://www.mass.gov/doc/covid-19-dashboard-april-26-2020/download))
5. Calculated (patients needing hospitalization/available hospital beds)
6. Changed calculations to percentages

## Load
### Our final database was exported to MongoDB and is named ETL_Output_Data.json.

We chose to export to MongoDB to gain more practice using the database management system. We recognize that a SQL system would be equally capable of handling this output and may actual be better in the long run for handling more complex queries.
