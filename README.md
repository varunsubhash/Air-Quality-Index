# AQI-Deployment

- In this project we collect weather and air quality index data from two different websites and try to and create  the dataset. We will finally create a model to predict the air quality index.

# Data Collection

- In this part the independent features are obtained from en.tutiempo.net. These contain the weather information.
- Its conatins the below data.</br>
   1 )T= Average temperature.</br>
   2 )TM = Maximum temperature.</br>
   3 )Tm = Minimum temperature.</br>
   4 ) SLP = Atmospheric pressure at sea level.</br>
   5 ) H = Average relative humidity.</br>
   6 ) VV = Avergae visibility.</br>
   7 ) V = Average wind speed.</br>
   8 ) VW = Maximum sustained windspeed.</br>
- In this model data for the city of Banglore is obtained for the period 2013-2018.
- We obtained the html for the all months in the above mentioned perod using the requests library.
- The data is then enocded to utf=8 and stored.
- The dependent feature is the air quality index score.
- Its obtained from a paid website weathermap.com.
- It contains data for every hour.
- We append the PM 2.5 data to a list.
- We remove data rows where we have Invalid,No data and pwr fail data.
- The PM 2.5 column data has data for every hour so we calculate the average value for each day.
- Now using the html files we web scrapp only the required data from the the web page using Beautiful Soup.



