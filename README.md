# PyBer_Analysis
## Project Overview
Analyzing ride share data for a fictional company "PyBer". Then creating charts to visualize the data using the Matplotlib library. Steps included:
  - Creating a bubble chart for ride-sharing data.
  - Calculating summary statistics for the ride-sharing data.
  - Creating a pie chart to visualize the percentage of total fares by city type (city types: Urban, Suburban, Rural).
  - Creating a pie chart to visualize the percentage of total rides by city type.
  - Creating a pie chart to visualize the percentage of total drivers by city type.
  
## Challenge
The challenge for this module involved creating three deliverables. They are:
  - A DataFrame summarizing the key metrics for ride-sharing data by city type (in the PyBer.ipynb file)
  - A multiple-line chart, with one line for each city type, that shows the sum of fares for each week (Total_Fare_by_City_Type.png in       the analysis folder).
  - A written report of the results (this starts below under "Challenge Summary").

## Challenge Summary
  The purpose of this assignment was to perform analysis on ride-share data for a fictional company: PyBer, in order to derive insights into the profitability of business activites in each type of city. For the summary statistics deliverable, I analyzed the data by finding the total rides, total drivers, total fares, average fare per ride, and average fare per driver for each city type, I then placed all of this information into a DataFrame where city type was the index. For the line graph, I organized the ride-share data into a pivot table where the date was the index, the city types were the columns, and the fares were summed by date and city type. I then graphed this information into a multiple-line chart where each line represents a different city type. The results from the summary statistics (the DataFrame is provided below) are as follows: urban cities had the highest number of rides, drivers, and total fares, but had the lowest average fare per ride and average fare per driver. Rural cities had the lowest number of total rides, total drivers, and total fares, but the highest average fare per ride and average fare per driver. Suburban cities were in the middle for all categories. The multiple-line chart (shown below) shows that the urban cities consistently had the largest total fare by month, followed by suburban cities, and lastly followed by rural cities. The results in general show the urban cities being overall the most profitable in absolute terms (total fares), but the rural cities being the most profitable in relative terms (average fare by driver/ride).
  
![](https://github.com/freddilly/PyBer_Analysis/blob/master/Summary%20Statistics.PNG)
![](https://github.com/freddilly/PyBer_Analysis/blob/master/analysis/Total_Fare_by_City_Type.png)

  In terms of challenges and difficulties faced, the main issue that I faced was in regards to changing the index data type for the DataFrame used for the multiple-line chart analysis from an object to datetime. For a while, I was having an issue changing the index to the datetime format, this was problematic as it would mean that I would be unable to resample the data by week for the chart analysis. I overcame this potential issue was making sure the data type of the index was correct (using pd.to_datetime), and ensuring that "Date" was set as the index for the pivot table. This allowed me to group the dates by week for the chart creation.
  
  Based on the data provided, there are several large disparities between the different city types. As seen previously, urban cities were the most profitable in terms of absolute measures, but fell well short of rural--and even suburban--cities in terms of relative measurements (average fare per ride and average fare per driver). The most logical explanation of this is probably that urban trips are generally shorter and thus cost less, thus causing the lower fare per ride figure. Also, the higher number of drivers in urban cities means that there is generally more competition between drivers to get fares, thus lowering the average fare per driver figure. In terms of further analyses, I would recommend investigating the fare per mile by city type, and the fare per minute by city type. This would allow PyBer leadership to get an accurate picture of the profitability by city type of each ride in terms of how long the rides are. The steps to perform this analysis are quite simple. These analyses require dividing the total fare by city type by the total amount of time spent driving by city type, and dividing the total fare by city type by the total distance driven by drivers in that city type. This would give an accurate representation of the profitability of rides in each city type.
  
