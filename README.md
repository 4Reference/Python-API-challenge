# Python-API
This is the repository for the Python API Homework.

## Exercises

### Weatherpy
Work completed in folder named same. From the Readme.md:

In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

Your first objective is to build a series of scatter plots to showcase the following relationships:
    Temperature (F) vs. Latitude
    Humidity (%) vs. Latitude
    Cloudiness (%) vs. Latitude
    Wind Speed (mph) vs. Latitude
After each plot add a sentence or too explaining what the code is and analyzing.

Your next objective is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):
    Northern Hemisphere - Temperature (F) vs. Latitude
    Southern Hemisphere - Temperature (F) vs. Latitude
    Northern Hemisphere - Humidity (%) vs. Latitude
    Southern Hemisphere - Humidity (%) vs. Latitude
    Northern Hemisphere - Cloudiness (%) vs. Latitude
    Southern Hemisphere - Cloudiness (%) vs. Latitude
    Northern Hemisphere - Wind Speed (mph) vs. Latitude
    Southern Hemisphere - Wind Speed (mph) vs. Latitude
After each pair of plots explain what the linear regression is modelling such as any relationships you notice and any other analysis you may have.

Your final notebook must:
    Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude.
    Perform a weather check on each of the cities using a series of successive API calls.
    Include a print log of each city as it's being processed with the city number and city name.
    Save a CSV of all retrieved data and a PNG image for each scatter plot.

#### Observations
For Part I, you must include a written description of three observable trends based on the data.
1)It may seem obvious, but sometimes it is good to use data to re-enforce standard knowledge. Based on Max Temp vs latitude it does seem that it generally gets warmer the closer one gets to the equator.

2)The lateral lines at specific break points in the cloudiness percentages (20%,40%,75%,90%) are likely due to rounding, guestimation and subjective metrics used to determine cloudiness. Meteorlogical standards seem to not use straight percentage:
"Cloud amount is reported in oktas or eighths with the additional convention that:
0 oktas represents the complete absence of cloud 1 okta represents a cloud amount of 1 eighth or less, but not zero 7 oktas represents a cloud amount of 7 eighths or more, but not full cloud cover 8 oktas represents full cloud cover with no breaks 9 oktas represents sky obscured by fog or other meteorological phenomena"

3)I thought humidity would have a more disperse pattern averaging around 50% but humidity at most latitudes seems to record at higher than 50%. So looking more into there is a washington post article about why we should stop using percent humidity to describe humidity and instead use relative humidity that is relative to temperature.

### Vacationpy
Work completed in folder named same. From the Readme.md:

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

Note: if you having trouble displaying the maps try running jupyter nbextension enable --py gmaps in your environment and retry.

Create a heat map that displays the humidity for every city from the part I of the homework.
#### Heatmap
Narrow down the DataFrame to find your ideal weather condition. For example:
    A max temperature lower than 80 degrees but higher than 70.
    Wind speed less than 10 mph.
    Zero cloudiness.
    Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.
    Note: Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.
Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

#### Hotel map

As final considerations:

Create a new GitHub repository for this project called API-Challenge (note the kebab-case). Do not add to an existing repo
You must complete your analysis using a Jupyter notebook.
You must use the Matplotlib or Pandas plotting libraries.
For Part I, you must include a written description of three observable trends based on the data.
You must use proper labeling of your plots, including aspects like: Plot Titles (with date of analysis) and Axes Labels.
For max intensity in the heat map, try setting it to the highest humidity found in the data set.
