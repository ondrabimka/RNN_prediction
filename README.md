# RNN_prediction

crypto_data directory contains my datasets. One os those files was downloaded and the others were created using "Crypto_dataset" script.

### Crypto_dataset.ipynb
Using this script I am downloading data from the last week.
It uses yfinance python library which allows me to download data form stock market into pandas dataframe.


### Crypto_prediction.ipynb
This file contains code for binary prediction -> It predicts if price is going to be higher or lower.
That file is mostly based on this tutorial: https://pythonprogramming.net/cryptocurrency-recurrent-neural-network-deep-learning-python-tensorflow-keras/. 
I also used dataset downloaded from there.


### Forecasting.ipynb
This is my main file now. In this case I was trying to predict exact future value. 
To properly create window I followed this very useful tutorial from tensorflow: https://www.tensorflow.org/tutorials/structured_data/time_series. 
Right now this script contains a lot of very simple models, but so far I have been focusing on (single step) LSTM GRU CNN networks (now I am trying to create bidirectionaly models GRU LSTM).

#### Personal observations.
##### For return_sequences=True
Generally basic GRU models have better performance on downloaded dataset than simple LSTM models. However, bidirectional models seem to have very similar performance so far.
Another thing which I found interesting was that when I added dropout performance got much worse. Maybe it is because my models are too small to. Could be worth using it with better models. Another thing that surprised me was that more layers did not always improved performance. 

##### For return_sequences=False
For this settings (on shot prediction) the best result was for basic LSTM and GRU and bidirectional has very similar result, which was a little bit worse than LSTM. 

