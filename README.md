# Python-APIs
UofM bootcamp python API homework

*WeatherPy:* 

Provided a cell to generate a list of cities based on randomly generated latitude/longitude values.

Built a dataframe of the cities and added empty weather data columns. OpenWeatherMap API called for each city to populate the weather data. Try/catch block used to catch exceptions where the city was not found by the API. Cleaned up the dataframe to remove cities not found and exported the data to output_Data/cities.csv file.

Matplotlib Scatterplots generated for each of the 4 relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude
The data is then split into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude) and plotted again (8 plots total). Each of the second plots has linear regression done on each relationship. As explained with each plot, few weather values show strong correlation to latitude. All plots saved as png.

*VacationPy:* 
Imports the cities.csv and use a google heatmap visualize the humidity for each city. 
The cities list is paired down using weather criteria to 8-12 cities with "ideal" vacation weather (future iteration of the code should include something that checks the U.S. State department site for viability of the vacation site). Vacation cities are put into new vacay dataframe. 
The Google Places API is used to find the hotels for each vacay city latitude/longitude using basic search criteria of lodging within 5k of the city with 'hotel' keyword.  try/catch block used to add first hotel result to the dataframe.  
Created new clean dataframe of cities the API successfully returned at least 1 hotel result.  
Pins for the clean dataframe cities are dropped over the google figure include a label with hotel name, city name and country code.

output_data folder contains the following:
* cities.csv - file created by weatherPy
* 12 Latitude vs <Weather feature> scatter plots
* heatMap_pointRadius1.PNG - screenshot of the heatmap before pins added.  This output was generated using a point radius of 1
* heatMap_pointRadius3_WithHotelPins.PNG - screenshot of heatmap including city/hotel pins.  This map was generated using a point radius of 3 for the heatmap layer.