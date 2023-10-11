# python-api-challenge

## Task

## Part 1: WeatherPy

Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

Create a Python script to visualize the weather of over 500 cities of varying distances from the equator. Use the citipy Python libraryLinks, the OpenWeatherMap APILinks, and problem-solving skills to create a representative model of weather across cities.

## Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude

Use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, create a series of scatter plots to showcase the following relationships:

Latitude vs. Temperature

Latitude vs. Humidity

Latitude vs. Cloudiness

Latitude vs. Wind Speed

## Requirement 2: Compute Linear Regression for Each Relationship

Compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). Define a function in order to create the linear regression plots.

Next, create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r values.

create the following plots:

Northern Hemisphere: Temperature vs. Latitude

Southern Hemisphere: Temperature vs. Latitude

Northern Hemisphere: Humidity vs. Latitude

Southern Hemisphere: Humidity vs. Latitude

Northern Hemisphere: Cloudiness vs. Latitude

Southern Hemisphere: Cloudiness vs. Latitude

Northern Hemisphere: Wind Speed vs. Latitude

Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

## Part 2: VacationPy

Use your weather data skills to plan future vacations. Use Jupyter notebooks, the geoViews Python library, and the Geoapify API.

The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.

Use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.

Create a map that displays a point for every city in the city_data_df DataFrame. The size of the point should be the humidity in each city.

Narrow down the city_data_df DataFrame to find your ideal weather condition.

Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.

For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

Add the hotel name and the country as additional information in the hover message for each city on the map

## Description

I started with the WeatherPy analysis with the jupyter notebook provided. I imported the necessary modules, API key, and citipy library. I ran the code provided to generate the cities list by using the citipy library. I moved on to retrieving the weather data from the OpenWeatherMap API by setting up the API base URL, creating an endpoint URL with each city, and parsing out latitude, longitude, max temp, humidity, cloudiness, wind speed, country, and date. I converted the cities weather data into a Pandas DataFrame.I created the scatter plots for lattitude vs. temperature, latitude vs. humidity, latitude vs. cloudiness, and latitude vs. wind speed. I defined a function to create the linear regression plots. Created a dataframe with northern and southern hemisphere weather data. I created the linear regression plots for temperature vs. latitude, humidity vs. latitude, cloudiness vs. latitude and wind speed vs. latitude for the northern and southern hemisphere DataFrames. I gave a short description of each of the linear regression plots and how the correlation of these various data points could be interpreted.

I started the VacationPy analysis with the jupyter notebook provided. I imported the necessary modules and API key. I loaded the CSV file from the city data DataFrame created in the first part. I created a map that displays a point for every city in the city_data_df DataFrame. The size of the point was determined by the humidity percentage in each city. I narrowed down the DataFrame to an example of ideal weather conditions. I dropped any of the null values and displayed a sample of the DataFrame. I created a copy of this newly created DataFrame to only have the city, country, coordinates, humidity and a blank column to store the hotel names in those cities. For each city, I used the Geoapify API to find the first hotel withing 10,000 metres of those coordinates. I set the radius and parameters. Got the longitude and latitude from the DataFrame. Added filter and bias parameters with the current city's latitude and longitude to the params dictionary. Set the base url, made an API request using the params dictionary, and converted the API to the json format. I configured and mapped this data to a map. I then added the hotel name and the country as additional infomrmation in the hover messasge for each city in the map.

