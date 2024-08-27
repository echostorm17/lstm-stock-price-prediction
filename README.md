# LSTM-Stock Price Prediction

# Table of Contents
- [What is LSTM?](#whatisLSTM)
    - [LSTM Cell](#LSTMCell)
    - [LSTM Forward Pass](#LSTMForward)
- [SAMPLE LSTM CODE: Prediction of Stock Prices Using LSTM network](#SampleStock)
- [References](#References)
  

## What is LSTM? <a name="whatisLSTM"></a>

- It is a special type of RNN, capable of learning long-term dependencies.

- "Long short-term memory (LSTM) units are units of a recurrent neural network (RNN). An RNN composed of LSTM units is often called an LSTM network. A common LSTM unit is composed of a cell, an input gate, an output gate and a forget gate. The cell remembers values over arbitrary time intervals and the three gates regulate the flow of information into and out of the cell"

- Long Short Term Memory (LSTM) is a type of deep learning model that is mostly used for analysis of sequential data (time series data prediction). 

- There are different application areas that are used: Language model, Neural machine translation, Music generation, Time series prediction, Financial prediction, Robot control, Time series prediction, Speech recognition, Rhythm learning, Music composition, Grammar learning, Handwriting recognition, Human action recognition, Sign Language Translation,Time series anomaly detection, Several prediction tasks in the area of business process management, Prediction in medical care pathways, Semantic parsing, Object Co-segmentation.

- LSTM was proposed in 1997 by Sepp Hochreiter and Jürgen Schmidhuber and improved in 2000 by Felix Gers' team.
[Paper](https://www.bioinf.jku.at/publications/older/2604.pdf) 

Code: https://github.com/omerbsezer/LSTM_RNN_Tutorials_with_Demo/tree/master/BasicLSTM

### LSTM Cell <a name="LSTMCell"></a>

<img width="886" alt="lstm_cell" src="https://user-images.githubusercontent.com/10358317/44312843-34a8bc80-a407-11e8-96c3-cc2bc07f1500.png">

[Andrew Ng, Sequential Models Course, Deep Learning Specialization]

### LSTM Forward Pass <a name="LSTMForward"></a>

<img width="860" alt="lstm_fw" src="https://user-images.githubusercontent.com/10358317/44312846-3a060700-a407-11e8-878e-f1ce14cc98b4.png">

[Andrew Ng, Sequential Models Course, Deep Learning Specialization]


## SAMPLE LSTM CODE: Prediction of Stock Prices Using LSTM network <a name="SampleStock"></a>
Stock and ETFs prices are predicted using LSTM network (Keras-Tensorflow).

Code: https://github.com/omerbsezer/LSTM_RNN_Tutorials_with_Demo/tree/master/StockPricesPredictionProject

- Stock prices are downloaded from [finance.yahoo.com](https://finance.yahoo.com/). [Disneyland (DIS) Stock Price CSV file](https://github.com/omerbsezer/LSTM_RNN_Tutorials_with_Stock_Prices_Prediction/blob/master/Stock_Prices_Prediction_Example/DIS.csv).
- Closed value (column[5]) is used in the network, [LSTM Code](https://github.com/omerbsezer/LSTM_RNN_Tutorials_with_Stock_Prices_Prediction/blob/master/Stock_Prices_Prediction_Example/pricePredictionLSTM.py)
- Values are normalized in range (0,1).
- Datasets are splitted into train and test sets, 50% test data, 50% training data.
- Keras-Tensorflow is used for implementation.
- LSTM network consists of 25 hidden neurons, and 1 output layer (1 dense layer).
- LSTM network features input: 1 layer, output: 1 layer , hidden: 25 neurons, optimizer:adam, dropout:0.1, timestep:240, batchsize:240, epochs:1000 (features can be further optimized).
- Root mean squared errors are calculated.
- Output files:  [lstm_results](https://github.com/omerbsezer/LSTM_RNN_Tutorials_with_Stock_Prices_Prediction/blob/master/Stock_Prices_Prediction_Example/lstm_result.csv) (consists of prediction and actual values), plot file (actual and prediction values).

![dis_prediction_and_actualprice](https://user-images.githubusercontent.com/10358317/37895737-e01ed832-30ea-11e8-9249-9b69ae2eccff.png)

## References: <a name="References"></a>
- [Andrew Ng, Sequential Models Course, Deep Learning Specialization](https://github.com/Kulbear/deep-learning-coursera/tree/master/Sequence%20Models)
- Basic LSTM Code is adapted from Andrew Ng's Course 'Sequential models'.