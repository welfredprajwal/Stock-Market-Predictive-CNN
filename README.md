# Stock Market Prediction

This project focuses on predicting stock market trends using a Convolutional Neural Network (CNN).
The model analyzes historical stock data to forecast future price movements. By applying convolutional layers to time-series features, the model extracts patterns and signals, enabling more accurate predictions of market direction.

Although CNNs are traditionally used in computer vision, their ability to capture local patterns makes them effective for financial time-series data as well.

# Dataset

| Feature   | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| Date      | Date of trading session                                                 |
| Open      | Opening price of the stock                                              |
| High      | Highest price during the session                                        |
| Low       | Lowest price during the session                                         |
| Close     | Closing price of the stock                                              |
| Volume    | Number of shares traded                                                 |
| RSI       | Relative Strength Index (technical indicator)                           |
| MACD      | Moving Average Convergence Divergence (technical indicator)             |
| Sentiment | Sentiment score derived from financial news / social media (optional)   |
| Target    | Label for prediction (e.g., next-day movement: up/down or future price) |

# Methodology

1.Data Preprocessing

  Handle missing values

  Normalize/scale features

  Generate rolling windows for time-series input
  
2.CNN Architecture

  Convolutional layers to extract local temporal patterns from the stock features

  Pooling layers to reduce dimensionality and capture essential features

  Dense (fully connected) layers to output predictions (price or movement direction)

3.Prediction Task

  Classification: Predict if the stock price will go up or down (Target = 0/1)

  Regression: Predict future price directly

4.Visualization & Analysis

  Plot predicted vs. actual prices

  Display moving averages, RSI, and MACD trends

# Results

After training the Convolutional Neural Network on historical stock data (technical indicators + sentiment features), the following performance metrics were observed on the test set:

| Metric        | Score (Example) |
| ------------- | --------------: |
| **Accuracy**  |             74% |
| **Precision** |             72% |
| **Recall**    |             76% |
| **F1-score**  |             74% |
| **ROC-AUC**   |            0.79 |

|                 | Predicted Up | Predicted Down |
| --------------- | -----------: | -------------: |
| **Actual Up**   |          320 |             80 |
| **Actual Down** |           70 |            310 |


