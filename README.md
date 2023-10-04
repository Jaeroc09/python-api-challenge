# python-api-challenge
Use of Python and APIs (OpenWeatherMap, Geoapify) to retrieve and analyze/visualize data

by Jason Estrada
#### Part 1: WeatherPy
A Python script was used to visualize the weather of over 500 cities of varying distances from the equator.  A randomized set of 1500 latitude/longitude coordinates was created, and the [citypy](https://pypi.python.org/pypi/citipy) library was used to generate a list of cities from these coordinates.  Weather information for these cities were captured using the [OpenWeatherMap API](https://openweathermap.org/api), and scatter plots were generated to determine if there were relationships for the following:
- Temperature vs Latitude
- Humidity vs Latitude
- Cloudiness vs Latitude
- Wind Speed vs Latitude

The city dataset was then split into northern and southern hemisphere subsets in order to perform additional analysis using linear regression.

Libraries used: matplotlib, pandas, numpy, scipy.stats, requests, time, datetime

#### Part 2: VacationPy
With the previously generated city dataset, a filter was applied for ideal weather conditions (subjective):
- City max temperature between 25-30 degrees C
- Cloudiness percentage of <= 20%

The nearest hotel information was pulled using the [Geoapify API](https://apidocs.geoapify.com/), and plotted with the [hvplot](https://hvplot.holoviz.org/index.html) library.

Libraries used:  hvplot, pandas, requests