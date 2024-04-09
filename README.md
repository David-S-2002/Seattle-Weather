# Using data to determine whether it rains more in Seattle or New York
The purpose of this project is to find out whether it rains more in Seattle or New York, by analyzing precipitation datasets from NOAA. The datasets have the daily precipitation in Seattle and New York, respectively, from January 1st, 2020 to January 1st, 2024.

## Data
The precipitation datasets were obtained from [NOAA's "Climate Data Online Search" page]( https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND).

## Data Preparation
I took the following steps to prepare the data:
- Inspecting the contents of the dataset
    - Using the head() and describe() functions to inspect the data
    - Checking that the column names are the same in both datasets
    - Checking the number of rows and stations in the dataset
- Converting the data types of the columns to the correct data types
- Removing unnecessary parts of the dataset
    - Removing unnecessary columns
    - Selecting only the data from the airport station in both cities (SeaTac in the Seattle data and JFK in the New York data)
    - Dropping duplicates
- Joining the SeaTac and JFK datasets
- Converting the DataFrame to a tidy (long) format
- Renaming the columns
- Identifying the missing data and performing linear interpolation
- Creating derived variables for the month and the year
- Exporting the clean dataset as a csv file

The file that performs the data preparation is data_preparation.ipynb. The clean data file is clean_seattle_nyc_weather.csv.
