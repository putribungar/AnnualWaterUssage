# AnnualWaterUssage
### Created by Putri Bunga Rahmalita
---------------------------------------------------------------------------------------
In this program I want to predict annual water usage year by year. Know the annual water use can be good for our earth, so we can save the earth by by using water as needed. Except that we can make program or movement to save water and save our earth.
<br><br>
The Dataset provides the annual water usage in Baltimore from 1885 to 1963, or 79 years of data. The values are in the units of liters per capita per day, and there are 79 observations. This dataset have 2 columns, which is Year and Baltimore city annual water use, liters per capita per day, 1885-1968.
<br>
<br>
I used ARIMA (AutoRegressive Integrated Moving Average) method to do time series analysis for analyzing time series data to extract meaningful statistics and other data characteristics. An autoregressive integrated moving average model is a form of regression analysis that gauges the strength of one dependent variable relative to other changing variables. The model's goal is to predict future securities or financial market moves by examining the differences between values in the series instead of through actual values.
<br>
<br>
An ARIMA model can be understood by outlining each of its components as follows:<br>
  - Autoregression (AR) refers to a model that shows a changing variable that regresses on its own lagged, or prior, values.<br>
  - Moving average (MA) incorporates the dependency between an observation and a residual error from a moving average model applied to lagged observations.<br>
  - Autoregression Moving average (ARMA) Sometimes stationary random processes have two characteristics of AR and MA. Random processes like this need to be approached with a mixed model between autoregressive and moving average average called ARMA (p, q).<br>
<br>
<br>
First, I load the dataset as a Pandas Series and split into two, one for model development (dataset.csv) and the other for validation (validation.csv). I split into 19 and 60 data because in ARIMA model I want to split data 50:50, so I just want the data more evenly and round. Then, I create summary of the dataset and create a plot of a time series dataset, to provide a lot of insight into the problem. I group the annual data by decade to observations for each decade. 
<br>
<br>
Next, I create models using ARIMA. First split the data, 50% of the dataset will be held back to train the model and 50% of the dataset will be iterated and test the model. When model trained, a one-step prediction made a the prediction stored. The actual observation from the test dataset will be added to the training dataset for the next iteration. Last, I calculate the RMSE using the helper function from the scikit-learn library to knowhow much the error/the model was wrong/gap between predection and expected value per capita per day for each prediction made.
<br>
<br>
For more details, please open my code, if there are questions feel free to ask me :)
