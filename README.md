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

## Data Analysis
I took the following steps to analyze the data:
- Compare the average amount of precipitation in Seattle and New York
    - Average the precipitation over all the months and years for each city
    - Average the precipitation each month for each city, and plot those averages
- Find out whether there more light rain events or heavy rain events in each city
    - Make a histogram of all the data that had a nonzero amount of precipitation
    - For each month, make a histogram of the data with a nonzero amount of precipitation
    - Make a 2D histogram with the month on the x-axis and the precipitation on the y-axis
- Find out how many rainy days there are in each month in each city
    - Count and plot the number of rainy days in each city during each month (for all the years)

The file that performs the data analysis is data_analysis.ipynb.
