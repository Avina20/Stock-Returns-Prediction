# Stock-Returns-Prediction
Stock market is viewed as tumultuous, mind boggling, unstable and dynamic. Without a doubt, its prediction is one of the most herculean task in time series prediction. Long short term memory (LSTM) networks are a best in class method for time series and sequence learning. Normally they are not applied to financial sequences, yet they are quite appropriate for this project. We used LSTM networks for forecasting the future stock prices from the historical prices, predict the stock returns and finally use binary classification to predict the direction of stocks.

## Data Acquisition
The data being used contains the daily stock prices for the Starbucks from February 2013 to February 2018. The data was acquired from the github repository of the account named lazyprogrammer. The dataset had the following features – date, open, high, low, close, volume and Name. The date stores the date for which the price is recorded. The stock market starts early in the morning and it stays open for the work day and closes. It changes throughout the day and so it is impossible to store an exact stock price. So the data stores the open price at the start of the day, in open; close price at the end of the day, in close; the maximum of the day in high, and the minimum of the day in low. The volume is the number of stocks that were traded that day. The name is the name of the stock company, i.e., Starbucks. 

## Architecture
The model is built on Tensorflow version 2.3.0.

The model is divided into three parts:
1.	Stock price prediction
2.	Stock returns prediction
3.	Directional classification

## Conclusion
We created three different models for predicting stock returns. Firstly, to predict future stock prices from past stick prices using LSTM, which worked well for single step forecast but it did not predict well for multi step forecast. It only copied the same values again and again. Second to predict stock returns with almost similar results as previous, and we also could not decrease loss much. Lastly to predict the direction of stocks(up/down) using binary classification on all the data. Even with these many data, the model still couldn’t perform any better than a random guessing. Hence there is no hope in the working of first two models as well.  If the model can’t even predict the up or down of the stocks, which is actually easier, then it definitely cannot predict the numerical values of the future stock prices or the returns from the future stocks. So it is impossible to make an almost perfect stock price forecast model. The fundamental flaw in our approach is using previous data to predict future data without considering the real world events. The stock prices depend on lot of real world factors like sensex, mood of investor, image of company, and it would be wrong to assume that the future is deterministic given the historical stock price trends.


