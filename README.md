# LSTM-Multivariate-Time-Series
## Demand Forecasting using LSTM 

Objective:
This project aims to forecast the demand forecasting for 12 weeks based on previous data and sale using LSTM. 

> The data has 144 rows and 131 columns. Feature engineering is a crucial part of this exercise to identify correct variables for forecasting. LSTM Multivariate Time Series technique is implemented using Keras. 


Important notes on LSTM(a type of RNN):
- processes inputs in a sequential manner
- remembers info which vanilla RNNs cannot
- retains long term dependency in sequential data
- RNNs suffer from problem of vanishing or exploding gradients 
- Gating mechanism in LSTM is what it sets apart, overcomes the problem of short term memory - preserves long term memory
- at each step, LSTM takes 3 parts of information :Current Input Data, Short term memory from previous cell (aka hidden state), Long term memory (aka cell state)
- Gates regulate the amount of information passes through 
- Input Gate has 2 layers : 1st layer uses hidden and current input through sigmoid. Sigmoid value lies betwwen 0 and 1 which tells how much info to keep or discard; weights of sigmoid updated in back propagation
- 2nd layer uses activation function on hidden and current input 
- combine these outputs --->>> information to be kept in long term memory 
- Forget Gate : Information to keep or discard from long term memory; multiply incoming long term memory by a forget vector
- LSTM uses sigmoid and tanh that are sensitive to magnitude so values need to be normalized


Source:
https://www.kaggle.com/competitions/sales-forecasting-time-series-prediction/overview
