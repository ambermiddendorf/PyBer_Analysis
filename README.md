# PyBer Analysis
Module 5 with Mathplotlib

## Overview of Analysis
#### Summarizing Ride-share Data by City Type
We'll be looking at the data from PyBer to compare the data from the three different city types - Rural, Suburban, and Urban. We'll summaryize the data by date and city type, looking at weekly data to give a line chart to compare the three city types and their total fares.

#### Creating the City Type Summary DataFrame
To create the City Type Summary DataFrame I created series for each Total Rides, Total Drivers, Total Fares, Average Fare per Ride, and Average Fare per Driver by grouping on the city type. I then joined those series into the summary DataFrame. I cleaned up the DataFrame and formatted the columns for easier reading.

#### Creating a Multi Line Plot to Show Weekly Fare by City Type
To create the line chart with total fare by week for each city type, I created a DataFrame with date as the index with the set_index function. I used that DataFrame to create a pivot table with Rural, Suburban, and Urban as the column headings, date as the rows, and total fares as the values. From that table, I located the data from 2019-01-01 to 2019-04-28, as directed. I then resampled the data by week to get weekly totals by city type. I then used Pandas to plot the line chart. 

## Results
#### PyBer Summary by City Type 
From the PyBer Summary by City Type DataFrame I see that as expected, Urban city types have the highest total rides, total drivers, and total fares. However, Urban cities do have the lowest average fare per ride and average fare per driver, as those are impacted by the Total Rides and Total Drivers numbers. I see that in Rural city types the average fare per ride and average fare per driver are higher than in Urban and Suburban cities, as the distances to travel are most likely further and the number of drivers are less, respectively. Suburban totals and averages fall right in between Rural and Urban city types.

![PyBerSummary](https://user-images.githubusercontent.com/95837693/151295538-d9832e20-f07b-4827-97ca-c231c8df11e3.JPG)

#### Total Fare by City Type
The Total Fare by City Type chart shows that the three city types' total fare by week do not follow the same trend. Some weeks Rural has peaks where Urban and Suburban have dips or flats and same for Urban and Suburban. They do all three see a slight peak the last week in February. 

![farebytype](https://user-images.githubusercontent.com/95837693/151295521-5ccf59f5-c5fc-4427-b68e-4ab29ae44c77.png)

## Summary
I believe the disparities you see among the city types' data shows the nature of each of those areas. Larger cities make for more demand in rides, but shorter rides, so you'll need more drivers in these cities to meet that demand. In the smaller cities, you won't need as many drivers, but your drivers will need to be willing to go further distances and therefore earn higher per ride fares. Based on the data from January through April, the fare trends do not look reliable enough to recommend more or less drivers during certain weeks/months. 
