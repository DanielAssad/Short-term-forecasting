# Short-term-forecasting
This repository provide a short-term prediction using Classical Statistical Models, Space-State Models and Machine Learning Models in R

The code starts calling necessary libraries and then converting databases available in the format required to run all forecasting models. 

Forecasting models available: Error, trend, Seasonal (ETS); Autoregressive Integrated Moving Avarage (ARIMA); Feed-forward neural networks with a single hidden layer and lagged inputs(NNETAR); Multi-layer perceptron (MLP); Exponential smoothing state space model with Trigonometric, Box-Cox transformation, ARMA errors, Trend and Seasonal components (TBATS); Kalman filter (KF) univariate and Multivariate; Vector Autoregressive (VAR).

The first aim is to select the best model in each class of model above mentioned. This selection is made considering Akaike Information Criterion (AIC).
Then the selected model is evaluated with three metrics described below:

1) In-sample: comparing training data with fitted values obtained;
2) Out-sample all: comparing all test data with predicted values obtained;
3) Out-sample mean: comparing a piece of test data (7 days ahead) with predicted values obtained 4 times and calculate the average error. We run the same model without parameters re-estimation, but we add a new week data (7 days).

The results are summarized in three dataframes (one for each metric presented) and then we properly choose the best model for each time series according to the lowest Root Mean Square Error (RMSE) criteria.

Finaly, after chose the best model to each time-series the "final" forecasting process is conduced.
