# GICS Sector Stock Price Predictor with LSTM

## Project Overview

### Problem
Stock market prices are inherently noisy and non-linear, making accurate short-term forecasting challenging. Traditional statistical models often fail to capture temporal dependencies in sequential financial data, especially across different industry sectors.

### Solution
This project leverages **Long Short-Term Memory (LSTM)** networks, a type of recurrent neural network (RNN), to learn time-based patterns in stock prices. Using daily closing prices of GICS sector ETFs (e.g., XLF for Financials), the models predict future movements with historical context.

### End Goal
To build a modular, reproducible pipeline for training, evaluating, and comparing LSTM models across multiple GICS sectors, aiding analysts and researchers in understanding sector-specific momentum and forecasting trends.

---

## Technologies Used

- **Pandas** – data wrangling  
- **NumPy** – numerical operations  
- **Matplotlib** – visualizations  
- **scikit-learn** – data preprocessing  
- **TensorFlow / Keras** – model building and training  
- **yfinance** – fetching historical stock data

---

## Notebook Overviews

### XLF – Financials Sector
Predicts stock prices of the **Financial Select Sector SPDR Fund (XLF)**.

- Uses past 100-day sequences to train the model
- LSTM network followed by a Dense output layer
- Evaluates predictions using RMSE and plots

---

### XLK – Technology Sector
Predicts movements for the **Technology Select Sector SPDR Fund (XLK)**.

- Deep LSTM with stacked layers and dropout
- Trained on normalized time-series data
- Outputs clear visual comparisons of actual vs predicted values

---

### XLRE – Real Estate Sector
Forecasts prices of the **Real Estate Select Sector SPDR Fund (XLRE)**.

- Historical price sequence modeling
- Dropout-enhanced LSTM architecture
- Evaluates overfitting via plot comparison

---

### XLV – Health Care Sector
Predicts trends in the **Health Care Select Sector SPDR Fund (XLV)**.

- Similar deep LSTM pipeline
- Performance evaluated with RMSE and visuals
- Highlights use of temporal patterns in health sector

---

## Coming Soon

-  **Dashboard** for comparing prediction results across sectors  
-  **Transformer-based models** for multi-sector attention modeling  
-  **Backtesting module** to simulate trading with predictions  
- Automated **report generation** for each sector’s performance  

