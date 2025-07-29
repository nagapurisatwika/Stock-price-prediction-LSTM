# Stock-price-prediction-LSTM
##  Project Overview

This project predicts future stock prices using historical data of **Apple Inc. (AAPL)** with the help of **LSTM (Long Short-Term Memory)** — a type of neural network that is well-suited for time series data. The dataset is automatically downloaded from **Yahoo Finance** using the `yfinance` Python library.
## 🚀 Technologies Used
- Python 🐍
- Keras & TensorFlow (for LSTM model)
- yfinance (for fetching stock data)
- scikit-learn (for data scaling)
- matplotlib (for plotting graphs)
- NumPy & Pandas (for data manipulation)

## 📂 Dataset
- **Source**: Yahoo Finance
- **Ticker**: AAPL (Apple Inc.)
- **Data Range**: From `2015-01-01` to `2024-01-01`
- **Feature Used**: Only the `Close` price

No CSV file is required. The data is fetched automatically.

---

## 📊 How the Model Works

1. **Fetch Data**: Use `yfinance` to download Apple's stock prices.
2. **Preprocess**:
   - Use only the 'Close' price.
   - Normalize it between 0 and 1 using `MinMaxScaler`.
   - Create sequences of past 60 days' prices to predict the next day's price.
3. **Build Model**:
   - Use a simple LSTM model with 2 LSTM layers and 1 Dense output layer.
4. **Train Model**:
   - Train on the past data using 10 epochs and batch size of 32.
5. **Predict**:
   - Predict stock prices using the trained model.
   - Reverse the scaling to get original values.
6. **Visualize**:
   - Plot actual vs predicted prices using `matplotlib`.


### 1. Install Required Libraries
```bash
pip install yfinance pandas numpy matplotlib scikit-learn tensorflow
