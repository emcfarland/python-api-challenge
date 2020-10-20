# python-api-challenge

This repository takes weather data from OpenWeather's API and returns data for random cities across the world.


## Analysis

The comparison of maximum temperature and latitude shows a strong negative correlation in the Northern Hemisphere and a strong positive correlation in the Southern Hemisphere, which makes sense intuitively given what we know about the sun's intensity at the equator and the poles. It also makes sense that they are not perfect matches since other factors like altitude and air currents could also affect temperature.

The comparisons of humidity, cloudiness, and wind speeds to latitude showed almost no correlation. The clustering of values at certain cloudiness percentages is intriguing, however. It would be interesting to see the methodolgy for calculating cloudiness, and if that methodolgy leads to the clumping or if it is purely coincidental.

The chosen regions for vacationing all landed at similar latitudes in the Northern and Southern Hemispheres. Because strict temperature restrictions were used, this adds further evidence to the idea that temperature and latitude are related.

