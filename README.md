# SBI Stock Price Prediction using LSTM

1. **Objective**:
   - The primary goal of this project is to predict the stock prices of SBI (State Bank of India) using historical stock price data and LSTM (Long Short-Term Memory) recurrent neural networks.
   
2. **Data Collection and Visualization**:
   - The historical stock price data for SBI is collected using the 'yfinance' library for the period from January 1, 2013, to December 31, 2018.
   - The data is visualized to gain insights into the stock price trends over time.
   - Only significant columns (Date, Open, High, Low, Close) are extracted to create the main dataset for training the LSTM model.

3. **Data Preprocessing**:
   - The data is preprocessed to prepare it for the LSTM model.
   - The 'MinMaxScaler' is used to scale the stock prices between 0 and 1, which is essential for better convergence during training.
   - A time window of 60 days is chosen for each data point in the training set. For each data point, the previous 60 days' stock prices are used as input features, and the next day's stock price is used as the target label.
   - The training set is split into input (X_train) and target (y_train) variables in the appropriate format required for LSTM.

4. **LSTM Model Building**:
   - A Sequential LSTM model is defined using the Keras library.
   - The model architecture consists of four LSTM layers, each followed by a Dropout layer to prevent overfitting.
   - The final layer is a Dense layer with one neuron to predict the next day's stock price.
   - The 'adam' optimizer and 'mean_squared_error' loss function are used for model compilation.

5. **Model Training**:
   - The LSTM model is trained using the training set (X_train and y_train).
   - The model is trained
