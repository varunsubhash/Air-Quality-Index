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
- We remove certain empty columns.
- All the data is written to the real_data file. This is the final data.

# Data Preparation

- Previously we deletd the empty columns.
- The independent and the dependent features are split to different variables.
- We check for null values and remove if any.

# Exploratory Data Analysis

- We use a pair plot to relation between different variables.
- The correlation function clearly  tells the magnitude of relation between them.
- A heat map can also di used to show it visually.
- Uisng tree regression we can find the feature importances very easily.
- By this we can see that Average visibility , Temperature has high negative corelation while Atmospheric pressure at sea level is has    high positive correlation.

# Modelling and Evaluation

- When applying we can see that we get very low scores for linear regression and even after using cross validation the results are not great.
- We are using 3 metrics
 1) Mean Absolute Error.
 2) Mean Square Error.
 3) Root Mean Square Error.
 
- We get the below results and we should minimize these as much as possible.</br>
 
  MAE: 40.28335537132939</br>
  MSE: 3057.664128674137</br>
  RMSE: 55.29614931144968</br>
 
 - The data is then stored in the pickle file.
 
 - Next we use Lasso Regression.
 - using Grid Search CV we get the below results.
 
  MAE: 40.15696946997222</br>
  MSE: 3103.2651026603376</br>
  RMSE: 55.706957399056876</br>
  
- This is not much better.

- Next we try use Decision Tree Regressor and we use Grid Search CV for hyper parameter tunning and we get the below results.

  MAE: 45.713945966514466</br>
  MSE: 4068.4996236840434</br>
  RMSE: 63.784791476370316</br>



