# Surfs Up!

## Overview
In this project I provided summary statistics of Oahu temperatures for the months of June and December.  To do so, I wrote two queries (one for each month) to retrieve the temperatures from the Measurement table, put the results into a list, converted the list into a dataframe and finally collected the statistics from the dataframe for additional analysis.

## Results
- The mean temperature for the month of June is 74.9 degrees, while the mean temperature for December is 71.0 degrees.  
- The standard deviation for June temperatures is 3.26 while the December standard deviation is 3.75.
- The median temperature for June is 75 degrees; December's is 71 degrees.  The minimum temperature recorded in June is 64 degrees, eight degrees warmer than December's minimum temp of 56 degrees.  The maximum temperature recorded in June is 85 degrees, only two degrees warmer than December's maximum temp of 83 degrees.

![June temp](https://github.com/MaxV6ft4/surfs_up/blob/main/June_Temps.png)
![Dec temp](https://github.com/MaxV6ft4/surfs_up/blob/main/Dec_Temps.png)

## Summary
Oahu has ideal surfing conditions year-round.  Despite the statistics displaying some minor differences, I believe they are negligible. The difference in standard deviation could partially result from a wider temperature range in December, but I think it is more a result of the difference in total recorded temperatures for each month (June has just under 200 additional recorded temperatures than December has).  The more recorded temperatures of similar degrees, the smaller the standard deviation.  Why assume the extra recorded temps are of similar degrees?  Because the first quartile (25%) is only two degrees lower than the median for both June and December.  Furthermore, the third quartile (75%) is two degrees higher than the median for June; three degrees higher than the median for December.  Therefore the extra recorded temps in June are almost certainly plus/minus one to two degrees from the median.

To obtain a better picture of the weather during June and December, I would write a similar query to the one above, only this time I would gather the precipitation data from the Measurement table in order to analyze the mean, median, and standard deviation of the amount of rainfall (Measurement.tobs would be replaced with Measurement.prcp in the query).  I'd personally predict more rainfall in December, but not enough to dampen surfers' spirits.  In addition, I'd write two more queries to gather both temperature and precipitation data from the two months but specifically from the most active station.  To do so I would filter the Measurement table twice, the second time to get the station (Measurement.station == 'USC00519281').
