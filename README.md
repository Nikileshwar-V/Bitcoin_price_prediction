# Bitcoin Price Prediction using Machine Learning

A machine learning-based project that predicts the next-day **Bitcoin price direction** (UP or DOWN) using historical price data and engineered financial features. This project uses real-time data from Yahoo Finance and applies a trained XGBoost classification model for inference.

---

## Project Overview

This project is part of my AI/ML journey, aimed at understanding crypto market trends using supervised learning. It predicts whether Bitcoin's **next-day closing price** will be higher or lower compared to today, based on features engineered from daily OHLC (Open, High, Low, Close) data.

---

## Key Features

- Fetches **real-time BTC-USD data** using `yfinance`
- Performs **feature engineering** (e.g., open-close, low-high, quarter-end flag)
- Scales input features using a trained `MinMaxScaler`
- Uses a **pre-trained XGBoost model** for prediction
- Prints output: 📈 Open | 📉 Close | 🔺 High | 🔻 Low | 🔮 Prediction: UP/DOWN

---

##  How It Works

1. Fetch the latest BTC-USD data for 1 day
2. Calculate:
   - `open_close = Close - Open` (daily sentiment)
   - `low_high = High - Low` (volatility)
   - `is_quarter_end = 1 if month in [3, 6, 9, 12] and day > 25 else 0`
3. Scale features using `MinMaxScaler`
4. Make prediction using a trained `XGBoostClassifier`
5. Display the result in human-readable format

---

## 📊 Feature Engineering

| Feature Name     | Description                                   |
| ---------------- | --------------------------------------------- |
| `open_close`     | Measures bullish or bearish sentiment         |
| `low_high`       | Indicates daily price volatility              |
| `is_quarter_end` | Flags end-of-quarter market anomalies         |

---

## Tech Stack

- **Python** 🐍
- **Scikit-learn** for scaling
- **XGBoost** for classification
- **Yahoo Finance API (yfinance)** for real-time BTC data
- **Pandas, Matplotlib** for EDA (in training phase)
- **Google Colab** for model training and testing

---

## Running the Project

### 1. Clone the repo

```bash
git clone https://github.com/Nikileshwar-V/Bitcoin_price_prediction.git
cd bitcoin-price-prediction

```
## install required files

pip install -r requirements.txt

## Example output

Open: 64250.12
Close: 64810.45
High: 65120.00
Low: 63900.10
Prediction for Tomorrow: ↑ UP

## Files in This Repo

| File                         | Description                                      |
| ---------------------------- | ------------------------------------------------ |
| `btc_price_prediction.ipynb` | Main Colab notebook with code and logic          |
| `btc_xgb_model.pkl`          | Trained XGBoost classification model             |
| `btc_scaler.pkl`             | Pre-fitted MinMaxScaler used for feature scaling |
| `README.md`                  | Project documentation (this file)                |

## Motivation
Understanding historical Bitcoin movements and identifying predictive signals using simple, interpretable features can build solid intuition for crypto-based AI applications and financial ML.

## Author
NIKILESHWAR.V
MCA Student | AI/ML Enthusiast | Open to Internships & Collaboration
📫 Connect with me: https://www.linkedin.com/in/nikileshwarv/



