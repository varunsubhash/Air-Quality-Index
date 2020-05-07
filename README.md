# AQI-Deployment

- In this project we collect weather and air quality index data from two different websites and try to and create  the dataset. We will finally create a model to predict the air quality index.

# Data Collection

- In this part the independent features are obtained from en.tutiempo.net. These contain the weather information.
- Its conatins the below data
   1 )T= Average temperature.
   2 )TM = Maximum temperature.
   3 )Tm = Minimum temperature.
   4 ) SLP = Atmospheric pressure at sea level.
   5 ) H = Average relative humidity.
   6 ) VV = Avergae visibility.
   7 ) V = Average wind speed.
   8 ) VW = Maximum sustained windspeed.
- In this model data for the city of Banglore is obtained for the period 2013-2018.
- We obtained the html for the all months in the above mentioned perod using the requests library.
- The data is then enocded to utf=8 and stored.
- The dependent feature is the air quality index score.
- Its obtained from a paid website weathermap.com.
- It contains data for every hour.
- 


