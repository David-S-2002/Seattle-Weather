# Using data to determine whether it rains more in Seattle or New York
The purpose of this project is to find out whether it rains more in Seattle or New York, by analyzing precipitation datasets from NOAA. The datasets have the daily precipitation in Seattle and New York, respectively, from January 1st, 2020 to January 1st, 2024.

## Data
The precipitation datasets were obtained from [NOAA's "Climate Data Online Search" page]( https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND).

## Data Preparation
I took the following steps to prepare the data:
- Inspecting the contents of the dataset (e.g.: checking that the column names are the same, checking how many weather stations are in each dataset)
- Converting the data types of the columns to the correct data types
- Removing unnecessary parts of the dataset (e.g.: removing unnecessary columns, picking only one station - the airport - from each city, dropping duplicates)
- Joining the Seattle (SeaTac airport) and New York (JFK airport) datasets
- Converting the DataFrame to a tidy (long) format
- Renaming the columns
- Identifying the missing data and performing linear interpolation
- Exporting the clean dataset as a csv file

The file that performs the data preparation is data_preparation.ipynb. The clean data file is clean_seattle_nyc_weather.csv.
