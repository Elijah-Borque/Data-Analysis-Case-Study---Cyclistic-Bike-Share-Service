A case study in which I conducted data analysis for a fictional bike share company called Cyclistic. 

This case study includes: 
  the case study scenario description document, 
  a deliverable summary document, 
  a URL link to the original data used, 
  an Excel Workbook containing the visualizations created for this case study, 
  and a PowerPoint presentation sharing the key insights and findings from this data analysis case study.

The cleaned data that was used for this case study could not be uploaded to GitHub due to file size restrictions, but the details of my data cleaning are provided below and in the deliverable summary document:

Some entries are missing information, including: the ride’s start station name, start station ID, end station name, end station ID. However, these entries do have starting latitudes and longitudes. These could possibly be attributed to customers using the bikes for their transportation, but deciding to not end their ride at a bike station. But there are duplicates of these longitudes and latitudes, which needs to be further investigated. For the sake of the business problem at hand, this information is not necessary at the moment.

Two columns were created for analysis: ride_length and day_of_week. The ride_length column is calculated by subtracting the column started_at from the column ended_at to get the duration of each ride. The day_of_week column is determined by using the WEEKDAY() function to attribute the date that each ride was started with a number to determine which day of the week the ride was done. For example, a 1 would mean the ride was done on a Sunday, 2 for Monday, and so on.

From these two columns, the following columns were created: avg_ride_length, max_ride_length, mode_day_of_week. The avg_ride_length column takes the mean of the ride_length column. The max_ride_length_column takes the maximum ride duration from the ride_length column. The mode_day_of_week takes the most frequent day value from the day_of_week column.

Some entries when calculating their ride_length, they came up as ######. This is because it was calculating a negative result due to the subtraction of a greater started_at value from a lower ended_at value. It is likely that the two values meant to be reversed, so to solve this issue, the equation for the ride_length column was modified to: =(D2-C2)*-1. This achieved the desired result for correctly calculating ride_length.


Conducted through the Google Data Analysis Certificate Course.
