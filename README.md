# Stock Price Prediction Using Linear Regression

This project fetches historical stock data for a specified symbol (default: AAPL) from Yahoo Finance, stores it in a MySQL database, engineers technical indicators as features, trains a Linear Regression model to predict adjusted closing prices, evaluates the model, and predicts the next day's stock price.

---

## Features

- Fetches historical stock data via `yfinance` API.
- Stores and updates data in a MySQL database.
- Creates lagged features, SMA, EMA, and RSI technical indicators.
- Trains a Linear Regression model using scikit-learn.
- Evaluates the model with MAE, MSE, RMSE, and R² metrics.
- Predicts the next day’s closing price based on recent data.

---

## Technologies & Libraries

- Python 3.x
- [yfinance](https://pypi.org/project/yfinance/) — for stock data fetching
- [mysql-connector-python](https://pypi.org/project/mysql-connector-python/) — for MySQL database interaction
- [pandas](https://pandas.pydata.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [numpy](https://numpy.org/)

---

## Setup & Installation

### Prerequisites

- Python 3.x installed
- MySQL Server installed and running
- Create a MySQL database (default in code: `hehe`)
- MySQL user with access privileges
- Git (to clone repo)

---

### Installation steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/stock-price-prediction.git
   cd stock-price-prediction

2. **Create and activate a virtual environment (optional but recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use: venv\Scripts\activate

3. **Install dependencies**

   ```bash
   pip install yfinance mysql-connector-python pandas scikit-learn numpy

4. **Configure database connection**
   Edit the following variables inside the script or create a config file:    
   DB_HOST = "your-db-host"
   DB_USER = "your-db-user"
   DB_PASSWORD = "your-db-password"
   DB_NAME = "your-db-name"
   STOCK_SYMBOL = "AAPL"  # Or any stock ticker symbol you want

5. **Run the script**
   ```bash
   python stock_price_prediction.py

## Output
Model evaluation metrics printed on the console (MAE, MSE, RMSE, R²).
Predicted next day closing price printed with date.
Database table updated with the latest data.

## Notes
Currently uses 1 year of data (period="1y"), but you can modify this in the fetch_stock_data() call for longer history (e.g., "5y").
Linear Regression model can be replaced with other ML models if desired.
Ensure MySQL server is running and accessible.
This project focuses on regression; it does not provide buy/sell signals.

## Contact
For questions or feedback, please contact:
Your Name — your.email@example.com
