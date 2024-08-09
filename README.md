# RNN
Predicting the Google Stock Price using LSTM

PS: Don't forget to upload the dataset (both Google_Stock_Price_Train.csv and Google_Stock_Price_Test.csv) into your Colab notebook by clicking the "Files" button on the left (the button looking like a folder) and then the "Upload" button. <br/>

The RNN I built was a regressor. Indeed, I was dealing with Regression because I was trying to predict a continuous outcome (the Google Stock Price). For Regression, the way to evaluate the model performance is with a metric called RMSE (Root Mean Squared Error). It is calculated as the root of the mean of the squared differences between the predictions and the real values. <br/>
However for the specific Stock Price Prediction problem, evaluating the model with the RMSE does not make much sense, since I am more interested in the directions taken by my predictions, rather than the closeness of their values to the real stock price. I want to check if my predictions follow the same directions as the real stock price and I don’t really care whether my predictions are close the real stock price. The predictions could indeed be close but often taking the opposite direction from the real stock price. <br/>
Nevertheless if you are interested in the code that computes the RMSE for our Stock Price Prediction problem, please find it just below: <br/>
     import math
     from sklearn.metrics import mean_squared_error
     rmse = math.sqrt(mean_squared_error(real_stock_price, predicted_stock_price)) <br/>
Then consider dividing this RMSE by the range of the Google Stock Price values of January 2017 (that is around 800) to get a relative error, as opposed to an absolute error. It is more relevant since for example if you get an RMSE of 50, then this error would be very big if the stock price values ranged around 100, but it would be very small if the stock price values ranged around 10000. <br/>
