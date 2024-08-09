# Google Stock Price Prediction Using Recurrent Neural Network (RNN)

## Overview

This project aims to predict Google's stock prices using a Recurrent Neural Network (RNN) built with LSTM (Long Short-Term Memory) layers. The model is trained on historical stock price data and attempts to forecast future prices, providing a visualization of both the real and predicted stock prices.

## Project Structure

- **Part 1 - Data Preprocessing:**
  - Import libraries and dataset.
  - Perform feature scaling using `MinMaxScaler`.
  - Create a data structure with 60 timesteps and 1 output for training.
  - Reshape the input data to be compatible with the LSTM model.

- **Part 2 - Building the RNN:**
  - Initialize the Sequential model.
  - Add LSTM layers with Dropout regularization to prevent overfitting.
  - Compile the model with the Adam optimizer and Mean Squared Error loss function.
  - Fit the model to the training data.

- **Part 3 - Making Predictions and Visualizing Results:**
  - Use the trained model to predict stock prices on test data.
  - Visualize the results by comparing the real and predicted stock prices using Matplotlib.

## Getting Started
## Prerequisites

Ensure you have the following libraries installed:

```
pip install numpy pandas matplotlib keras scikit-learn

```

## Running the Code

### Data Preprocessing:
- Load the training dataset and apply feature scaling.
- Prepare the training set with the appropriate timesteps.

### Model Training:
- Build the RNN model using LSTM layers.
- Train the model on the preprocessed data.

### Prediction and Visualization:
- Load the test dataset and predict the stock prices using the trained model.
- Visualize the real vs predicted stock prices.

## File Descriptions
- **Google_Stock_Price_Train.csv**: Training dataset with historical stock prices.
- **Google_Stock_Price_Test.csv**: Test dataset to evaluate the model's predictions.

## Results
- The model predicts Google's stock prices with a certain degree of accuracy, visualized in the form of a line plot comparing real and predicted values.
- The red line represents the real stock prices, while the green line shows the predicted prices.

## Future Work
- Experiment with different architectures and hyperparameters to improve prediction accuracy.
- Explore other types of neural networks or machine learning models for stock price prediction.
- Apply the model to other financial datasets.
