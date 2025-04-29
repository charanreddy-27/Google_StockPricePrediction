# 📈 Google Stock Price Prediction using LSTM and PyTorch

Predicting the future stock prices of **Google (GOOG)** using deep learning techniques — powered by **LSTM** models built with **Keras** and **PyTorch**.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Project Workflow](#project-workflow)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Results](#results)
- [Challenges & Solutions](#challenges--solutions)
- [Conclusion](#conclusion)
- [Installation & Usage](#installation--usage)
- [License](#license)

---

## 🧠 Overview

This project forecasts Google's stock prices using historical market data and advanced machine learning techniques. By leveraging **LSTM networks**, we model the temporal nature of stock market data to predict future prices with improved accuracy.

---

## ⚙️ Tech Stack

- Python
- PyTorch
- Keras / TensorFlow
- NumPy, Pandas
- Matplotlib, Seaborn
- yFinance
- Scikit-learn
- Plotly (for advanced visualizations)

---

## 🔁 Project Workflow

### 📥 1. Data Collection & Preprocessing
- Fetch historical stock data using `yfinance`.
- Handle missing values, convert data types.
- Normalize features using `MinMaxScaler`.

### 📊 2. Exploratory Data Analysis (EDA)
- Identify trends, patterns, and seasonality.
- Heatmaps, violin plots, pair plots, and box plots used for analysis.

### 🛠 3. Feature Engineering
- Added **Simple Moving Averages** (10, 20, 50 days).
- Calculated **daily returns** for volatility insights.

---

## 🤖 Model Building

### Option 1: LSTM with **Keras**
- Built and trained an LSTM model using the Keras API.
- Implemented early stopping and dropout layers.

### Option 2: LSTM with **PyTorch**
- Built a custom LSTM from scratch in PyTorch.
- Used custom training loops and evaluation functions.

---

## 📏 Model Evaluation

- Metrics: **Mean Squared Error (MSE)** for performance evaluation.
- Plotted loss curves for both models.
- Compared **predicted vs actual** values using line and candlestick charts.

---

## 📊 Results

| Model      | MSE Score | Notes                       |
|------------|-----------|-----------------------------|
| Keras LSTM | ✅ Lower   | Better generalization       |
| PyTorch LSTM | Slightly higher | Customizable and transparent |

- Models accurately captured short-term trends.
- Predictions shown for **next 10 days** with visual comparison.

---

## ⚠️ Challenges & ✅ Solutions

| Challenge | Solution |
|----------|----------|
| Data Quality & Scaling | Used `MinMaxScaler`, cleaned missing values |
| Feature Selection | Added moving averages, daily returns |
| Overfitting | Dropout layers, early stopping |
| Architecture Tuning | Tried different LSTM configurations |

---

## 🧾 Conclusion

This project demonstrates how deep learning, specifically LSTM networks, can be effectively applied to **financial time-series forecasting**. Both models provided meaningful predictions and opened insights into stock market behaviors.

---

## 🚀 Installation & Usage

```bash
# Clone the repository
git clone https://github.com/yourusername/google-stock-lstm.git
cd google-stock-lstm

# Create and activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the project
python main.py
