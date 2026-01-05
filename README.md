# stock_price_prediction_ml.py
Stock price direction prediction using machine learning models (Logistic Regression, SVM, and XGBoost) with feature engineering and performance evaluation.
# Stock Price Prediction Using Machine Learning

This project implements multiple **machine learning models** to predict the **next-day stock price direction** using historical stock market data.  
The workflow includes **exploratory data analysis (EDA)**, **feature engineering**, **model training**, and **performance evaluation**.

---

##  Project Objective

To predict whether a stock’s **closing price will increase or decrease the next trading day** using machine learning classification techniques.

---

##  Dataset

- Stock price dataset in CSV format  
- Example used: **Tesla.csv**
- Required columns:
  - Date
  - Open
  - High
  - Low
  - Close
  - Adj Close (removed during processing)
  - Volume

---

##  Technologies & Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

##  Exploratory Data Analysis (EDA)

- Time-series plot of closing prices
- Distribution plots for numerical features
- Boxplots to detect outliers
- Correlation heatmap
- Year-wise average price analysis

---

##  Feature Engineering

The following features are created:
- `day`, `month`, `year` (from Date column)
- `is_quarter_end` (quarter-end indicator)
- `open-close` = Open − Close
- `low-high` = Low − High

### Target Variable
- `1` → Next day closing price increases  
- `0` → Next day closing price decreases

---

## Data Preprocessing

- Feature scaling using **StandardScaler**
- Train-validation split:
  - Training set: 90%
  - Validation set: 10%

---

##  Models Used

- Logistic Regression
- Support Vector Machine (Polynomial Kernel)
- XGBoost Classifier

---

##  Model Evaluation Metric

- **ROC-AUC Score** used for:
  - Training performance
  - Validation performance

---

##  How to Run the Project

1. Clone the repository
2. Install required dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn xgboost
3. Update the dataset path in the script
4. Run the file:
   ```bash
   python stock_price_prediction_ml.py

---

## Results

The project compares the performance of different machine learning models and highlights their ability to predict stock price direction effectively.

---

## Future Enhancements

- Hyperparameter tuning
- Cross-validation
- Inclusion of technical indicators (RSI, MACD, Moving Averages)
- Backtesting trading strategies
- Support for multiple stock datasets

---

