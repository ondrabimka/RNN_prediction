# RNN_prediction

crypto_data directory contains some of my datasets. One os those files was downloaded and the others were created using "YFinance_data.ipynb" and "Binance_data.ipynb" script.

### YFinance_data.ipynb
Using this script I am downloading data from the last week.
It uses yfinance python library which allows me to download data form stock market into pandas dataframe. Unfortunatelly when obtaining 1 minute data only 1 week into the past is possible

### Binance_data.ipynb
This script donwloads all selected pairs from Binance. It is necessay to have a Binance account and with API turned on. For easier communication I used following library https://python-binance.readthedocs.io/en/latest/. 

### Crypto_prediction.ipynb
This file contains code for binary prediction -> It predicts if price is going to be higher or lower.
That file is mostly based on this tutorial: https://pythonprogramming.net/cryptocurrency-recurrent-neural-network-deep-learning-python-tensorflow-keras/. 
I also used dataset downloaded from there.

### Forecasting.ipynb
This is my main file now. In this case I was trying to predict exact future value. 
To properly create window I followed this very useful tutorial from tensorflow: https://www.tensorflow.org/tutorials/structured_data/time_series. 
Right now this script contains a lot of very simple models, but so far I have been focusing on (single step) LSTM GRU CNN networks (now I am trying to create bidirectionaly models GRU LSTM).

### Forecasting-big-model.ipynb
Basically the same file as "Forecasting.ipynb", but here I trained models on more bigger dataset which also included more cryptocurrencies (those were selected based on some data exploration which could be found in "Data_explore.ipynb"). In those bigger models I used 30 minutes to predict 1 minute into the future.  

### Data_explore.ipynb
This file contains data exploration of crypto data available on Binance (graphs and info). I tried to create the best dataset from most correlated cryptocurrencies. I also tried to plot and explore various normalising strategies. 

##### Example of correlated and uncorrelated data from Data_explore file.
![image](https://user-images.githubusercontent.com/47148499/127770334-af230fb0-b7b6-4c2a-bb04-4c1e923b86d0.png)


### Model_playground.ipynb
This file contains visualized predictions, calculated MAE and percantage of correct directions of all models. All scores from this file are included in models_comparsion.xlsx.

##### Example of predictoins made by models from Model_playground file.
![image](https://user-images.githubusercontent.com/47148499/128783090-428a246d-0535-4529-a405-1faed63f9def.png)

### NN_plots.ipynb
Contains plots and comparsion tables used in my work. Plotted data is usually from models_comparsion.xlsx.

##### Example of plot from NN_plots.
![image](https://user-images.githubusercontent.com/47148499/128783111-41f22b57-3ecb-4a71-a64e-66d4fe1a216e.png)


### Models_comparsion.xlsx
In this file I saved all scores with corresponding architectures and compile settings. (Note: some some scores are empty because for some reason they were not necesary) 

![model_expl](https://user-images.githubusercontent.com/47148499/127777576-c0c4ecc5-1c92-40de-9567-41960a0fc7dc.png)



