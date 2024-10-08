<div align="center">
  <img src="https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/Logo.png"><br><br>
</div>


**Neural-Net-with-Financial-Time-Series-Data** is an open source software project for neural network to predict daily log return of any financial asset. The project includes a parsimonious rule-based Model for Sentiment Analysis for the New York Times and serveral technical indicators (ie. Stochastics, Moving Average Convergence/Divergence oscillator) to train a LSTM neural network by stochastic gradient descent with warm restart(SGDR) and cosine annealing. This flexible architecture enables you to deploy with Nvidia CuDNN computation without rewriting code by yourself.  


## Latest Result:

The current LSTM model result for predicting daily log return.

![Alt text](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/Predicted_vs_True_all_last%20300.png)


## Old model Result

This old model uses LSTM to predict stock price.

![Alt text](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/20170510result.png)


## LSTM cell 

This is the LSTM cell we used in the model.

![Alt text](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/lstm.png)

It is **faster** than normal LSTM cell because of the implementation of CuDNN LSTM and batch normalization in the model.

## Stochastic Gradient descent with restart (SGDR)

![](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/SGDR.png)

The figure is from the paper snapshot ensembles, which uses each iteration as a new ensemble model.

## Update:
1. Recurrent neural network with LSTM is added to the code. 
2. Keras with tensorflow is also implemented. 
3. Tensorboard for neural network visualization is also added to the code.

1. Normalized adjusted close price. 
2. A new data downloader has been implemented for simplicity
3. Added more variable to predict the adjusted close price
4. More accurate result, significantly less mean square error
5. Extra visualization for close price
6. Denormalization will be fixed soon
7. Twitter sentiment analysis is currently on testing stage

1. Updated denormalization 
2. More test results available

1. Updated fundamental data from Kaggle for NYSE 

1. Supporting Python 3.5 on Windows 10
2. Significant improvement in accuracy

1. ^GSPC Data since 1970 has been added, more training data, higher accuracy
2. 7 years of test data 
3. Object oriented programming
4. Hyperparameters for dropout has been tested

1. All Hyperparameters have been tested and results have been uploaded.
2. Fixed comment for the data loader
3. More technical analysis like volume, moving average and other indexes will be added

1. Using Quandl instead of Pandas datareader
2. Correlation heatmap has been addded
3. Using Adjusted OHLCV for the network
4. All functions can be loaded from lstmstock.py
5. A Quandl api key is provided temporarily for those who do not own a quandl account
6. Moving averages have been added


![Alt text](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data/blob/master/Photos/Dataframe.png)

1. Event driven analysis
2. Switched to Tensorflow LSTM model
 
1. Complete rewrite of News downloader, removed Newsapi in order to get full access to NYTImes data for free
2. Moving Average Convergence/Divergence oscillator (MACD), Stochastic Oscillator, Average True Range are added to train the model.
3. log return is now used as target variable. 
4. Keras on top of Tensorflow is used.
5. Randomized Search from SKLearn is used for optimization.

Serveral state of the art techniques are applied
1. CuDNN LSTM is used to accelerate training
2. Stochastic gradient descent with warm restart
3. Cosine annealing 
4. Neat splitting method
5. Dataset is provided 
6. HDF files are used to accelerate reading time

## Future update
1. Bayesian search will be used to optmize hyperparameters.
2. Deep Feature Synthesis will be used for auto feature engineering.
3. Quantopian zipline will be used for backtesting the model.

## References:
Bernal, A., Fok, S., & Pidaparthi, R. (2012). Financial Market Time Series Prediction with Recurrent Neural Networks.

Box, G. E., Jenkins, G. M., Reinsel, G. C., & Ljung, G. M. (2019). Time series analysis: forecasting and control. John Wiley & Sons.

Gu, J., Wang, Z., Kuen, J., Ma, L., Shahroudy, A., Shuai, B., ... & Cai, J. (2019). Recent advances in convolutional neural networks. arXiv preprint arXiv:1512.07108.

Hutto, C.J. & Gilbert, E.E. (2017). VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text. Eighth International Conference on Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.

Jaeger, H. (2001). The “echo state” approach to analysing and training recurrent neural networks-with an erratum note. Bonn, Germany: German National Research Center for Information Technology GMD Technical Report, 148(34), 13.

Jaeger, H. (2002). Tutorial on training recurrent neural networks, covering BPPT, RTRL, EKF and the" echo state network" approach (Vol. 5). GMD-Forschungszentrum Informationstechnik.

Maass, W., Natschläger, T., & Markram, H. (2002). Real-time computing without stable states: A new framework for neural computation based on perturbations. Neural computation, 14(11), 2531-2560.
