# 📈 TCS Stock Price Prediction using Machine Learning & LSTM







### 📌 Project Overview

This project performs historical stock data analysis and price prediction for Tata Consultancy Services (TCS) using both:

**Traditional Machine Learning (Linear Regression)**

**Deep Learning (LSTM – Long Short-Term Memory)**

The objective is to analyze stock price behavior and build predictive models capable of forecasting future closing prices based on historical trends.

### 🎯 Objectives

- Analyze historical stock price patterns

- Perform exploratory data analysis (EDA)

- Engineer time-series features

- Build and compare predictive models

- Evaluate performance using appropriate metrics

### 🗂 Dataset Description

The dataset contains historical daily trading data of TCS stock with the following features:

| Feature      | Description              |
| ------------ | ------------------------ |
| Date         | Trading Date             |
| Open         | Opening Price            |
| High         | Highest Price of the Day |
| Low          | Lowest Price of the Day  |
| Close        | Closing Price            |
| Volume       | Number of Shares Traded  |
| Dividends    | Dividend Information     |
| Stock Splits | Stock Split Data         |


### 🛠 Tech Stack

**Programming Language:** Python

**Data Processing:** Pandas, NumPy

**Visualization:** Matplotlib, Seaborn

**Machine Learning:** Scikit-learn

**Deep Learning:** TensorFlow / Keras

**Environment:** Jupyter Notebook

## 📊 Project Workflow
#### 1️⃣ Data Preprocessing

Converted Date column to datetime format

Sorted dataset chronologically

Handled missing values using forward fill

#### 2️⃣ Exploratory Data Analysis (EDA)

Close price trend visualization

Correlation heatmap analysis

Volume and price behavior analysis

Volatility observation using daily returns

#### 3️⃣ Feature Engineering

Created time-series relevant features:

Daily Percentage Return

Previous Day Closing Price (Lag Feature)

These features help capture market momentum and temporal dependency.

#### 4️⃣ Linear Regression Model

Features Used: Open, High, Low, Volume, Prev_Close

Target Variable: Close Price

Evaluation Metrics:

Mean Squared Error (MSE)

R² Score

Linear Regression establishes a baseline model performance.

#### 5️⃣ LSTM Deep Learning Model

Since stock prices are sequential and time-dependent, an LSTM model was implemented.

Steps:

- Selected Close price

- Scaled data using MinMaxScaler

- Created sequential input-output pairs

- Performed chronological 80/20 train-test split

- Trained LSTM model

- Evaluated using Mean Absolute Error (MAE)

### 📈 Model Comparison

| Model             | Type           | Strength                         |
| ----------------- | -------------- | -------------------------------- |
| Linear Regression | Traditional ML | Captures linear relationships    |
| LSTM              | Deep Learning  | Captures sequential dependencies |


LSTM demonstrates better capability for modeling time-series behavior due to its memory mechanism.

### 🚀 How to Run the Project

**1️⃣ Clone the repository:**

git clone <your_repository_link>

**2️⃣ Install required libraries:**

pip install pandas numpy matplotlib seaborn scikit-learn tensorflow

**3️⃣ Launch Jupyter Notebook:**

jupyter notebook

**4️⃣ Run all cells sequentially.**

### 📌 Key Learnings

Time-series data must be split chronologically to prevent data leakage.

Scaling is essential for neural networks.

LSTM models require sequence creation for supervised learning.

Deep learning performs better when modeling temporal dependencies.

### 🔮 Future Enhancements

Multi-step forecasting (Next 7–30 days prediction)

Hyperparameter tuning

ARIMA / SARIMA comparison

Real-time stock prediction using APIs

Deployment using Streamlit