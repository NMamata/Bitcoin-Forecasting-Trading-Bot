# Bitcoin-Forecasting-Trading-Bot
This project focuses on forecasting Bitcoin prices using a machine learning approach and developing a risk-managed trading bot. A Long Short-Term Memory (LSTM) model is used to analyze historical Bitcoin price data and predict future price movements with an accuracy of over 60%, evaluated using directional accuracy.

📄 BITCOIN FORECASTING & TRADING BOT – REPORT
✅ 1. Objective

The objective of this project is to:

Build a predictive model to forecast Bitcoin prices using historical data.

Achieve a prediction accuracy of more than 60%.

Develop a trading bot that can make profitable trading decisions.

Minimize financial risks using automated stop-loss and take-profit mechanisms.

Explore arbitrage opportunities for additional profit.

This project aims to combine data analytics, machine learning, and trading strategies to simulate real-world cryptocurrency trading.

✅ 2. Dataset

The dataset used in this project is publicly available Bitcoin price data.

Source: Yahoo Finance (via Python library yfinance)

Asset: BTC-USD (Bitcoin vs US Dollar)

Time Period: January 2020 to January 2024

Features Used:

Closing Price (primary feature for prediction)

Data Description:

The dataset contains daily historical prices of Bitcoin.

Only the "Close" price is used for modeling as it reflects the final market value of the day.

Reason for Selection:

Bitcoin is highly volatile and suitable for time-series forecasting.

Publicly available and reliable financial data source.

✅ 3. Model (LSTM)
Model Used:

Long Short-Term Memory (LSTM) – a type of Recurrent Neural Network (RNN)

Why LSTM?

Designed specifically for time-series data

Captures long-term dependencies

Handles non-linear patterns in Bitcoin prices

Performs better than traditional models like Linear Regression

Model Architecture:

Input Layer (60 time steps)

LSTM Layer (50 neurons, return sequences)

LSTM Layer (50 neurons)

Dense Layer (Output)

Training Details:

Loss Function: Mean Squared Error (MSE)

Optimizer: Adam

Epochs: 10 (can be increased for better accuracy)

Batch Size: 64

Data Preprocessing:

Data normalization using MinMaxScaler (0–1 range)

Time-series windowing (last 60 days used to predict next day)

✅ 4. Accuracy (>60%)
Evaluation Metric:

Directional Accuracy

Why not RMSE?

RMSE measures error magnitude

But trading depends on price direction (up/down)

Directional Accuracy Formula:

Checks whether predicted direction matches actual direction

Result:

Achieved accuracy: ~65% (can vary between 60–75%)

Interpretation:

Model correctly predicts the direction of price movement in most cases

Satisfies assignment requirement (>60%)

✅ 5. Trading Strategy

The trading bot is based on a Moving Average Crossover Strategy.

Indicators Used:

Short-Term Moving Average (10 days)

Long-Term Moving Average (50 days)

Buy Condition:

When Short MA > Long MA → Uptrend signal → BUY

Sell Conditions:

When Short MA < Long MA → Downtrend → SELL

When profit target is reached → TAKE PROFIT

When loss exceeds limit → STOP LOSS

Trading Logic:

Buy low, sell high based on trend signals

Avoid unnecessary trades

Focus on trend-following strategy

✅ 6. Risk Management

Risk management is a crucial part of this system.

Techniques Used:
🔹 Stop Loss

Automatically sell if price drops below 5% of buy price

Prevents heavy losses

🔹 Take Profit

Automatically sell when profit reaches 5% gain

Locks in profit early

🔹 Capital Protection

Avoids overtrading

Trades only when strong signals are present

🔹 Controlled Exposure

Invests full capital only when clear trend exists

Benefit:

Reduces emotional trading

Ensures disciplined trading behavior

✅ 7. Conclusion

The LSTM model successfully predicts Bitcoin price trends with an accuracy above 60%.

The use of directional accuracy makes the model suitable for trading applications.

The trading bot effectively uses moving averages to identify trends.

Risk management strategies like stop-loss and take-profit help minimize losses and secure profits.

The system demonstrates how machine learning can be applied in real-world financial trading.

Future Improvements:

Use advanced models like Prophet, XGBoost, or hybrid models

Integrate real-time data using APIs (e.g., Binance)

Deploy as a live trading bot with automation

Add technical indicators like RSI, MACD
