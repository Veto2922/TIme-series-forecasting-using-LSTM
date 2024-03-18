# Recurrent Neural Network for Stock Price Prediction

This notebook implements a Recurrent Neural Network (RNN) to predict Google stock prices using historical data. The RNN model is built using Long Short-Term Memory (LSTM) units, a type of recurrent neural network architecture well-suited for sequence prediction tasks.

## Part 1 - Data Preprocessing
### Importing the libraries
- `numpy`: For numerical computations.
- `matplotlib`: For data visualization.
- `pandas`: For data manipulation and analysis.

### Data Import and Preprocessing
1. **Importing the training set**: The historical Google stock price data for training is loaded from a CSV file.
2. **Feature Scaling**: The training data is scaled using Min-Max scaling to normalize the values within a range (0, 1).
3. **Creating data structure**: Sequences of 60 previous stock prices are created as input features along with the next day's stock price as the output label.

## Part 2 - Building and Training the RNN
### Model Architecture
1. **Initialization**: A Sequential model is initialized using Keras.
2. **LSTM layers**: Four LSTM layers are added with dropout regularization to prevent overfitting.
3. **Output layer**: A Dense layer is added to produce the predicted stock price.
4. **Compilation**: The model is compiled with Adam optimizer and Mean Squared Error loss function.
5. **Training**: The model is trained on the training data with 100 epochs and a batch size of 32.

## Part 3 - Making Predictions and Visualization
### Prediction Process
1. **Data Preparation**: The test dataset is loaded, and input sequences are created similar to the training set.
2. **Prediction**: The trained model is used to predict the stock prices for the test data.
3. **Inverse Scaling**: Predicted prices are inverse transformed to obtain the actual stock prices.
4. **Visualization**: Real and predicted stock prices for the test period (2017) are plotted to visualize the model's performance.

## Files Required
- `Google_Stock_Price_Train.csv`: CSV file containing the training data.
- `Google_Stock_Price_Test.csv`: CSV file containing the test data.

Ensure these files are available in the same directory as the notebook for proper execution.

This notebook provides a comprehensive guide to build, train, and evaluate an RNN model for stock price prediction using LSTM architecture.
