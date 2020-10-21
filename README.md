# python-api-challenge

This repository takes weather data via API and does analyses to determine whether or not latitude will affect the weather and to pick "the perfect vacation spot."

WeatherPy uses the citipy module and OpenWeather's API to compile weather data for 500+ random cities across the world. These data are stored in a pandas dataframe and saved as a CSV, and several series are plotted in matplotlib scatter plots to tease out any relationships in the data. Lastly, regression lines are overlaid and r-squared values are calculated to determine the correlation between weather information and latitude for the Northern and Southern Hemispheres.

VacationPy uses the gmaps module and Google Places API to plot the locations of potential vacation spots. The script reads the csv saved in WeatherPy and narrows it down to around 10 cities by placing weather restrictions on the data. Then, those locations are called with the Places API and the first hotel within 5000 meters is returned. FInally, those hotels and corresponding cities and countries are placed as markers on a heatmap weighted by humidity.

## Analysis

The comparison of maximum temperature and latitude shows a strong negative correlation in the Northern Hemisphere and a strong positive correlation in the Southern Hemisphere, which makes sense intuitively given what we know about the sun's intensity at the equator and the poles. It also makes sense that they are not perfect matches since other factors like altitude and air currents could also affect temperature. The chosen regions for vacationing all landed at similar latitudes in the Northern and Southern Hemispheres. Because strict temperature restrictions were used, this adds further evidence to the idea that temperature and latitude are related.

The comparisons of humidity, cloudiness, and wind speeds to latitude showed almost no correlation. This suggests that latitude is not related to those metrics, which one could hypothesize might relate more to geological features.

The clustering of values at certain cloudiness percentages is intriguing. It would be interesting to see the methodolgy for calculating cloudiness, and if that methodolgy leads to the clustering or if it is purely coincidental.
