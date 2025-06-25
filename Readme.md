# 🏏 IPL Auction Data Analysis & Prediction

This project performs **data analysis and machine learning modeling** on IPL auction data to understand player trends, team spending behavior, and predict future auction outcomes such as **winning bid amounts** and **team classifications**.

## 📁 Dataset Overview

- The dataset (`final_dataset.csv`) contains historical IPL auction data, including:
  - Player names
  - Teams
  - Base prices
  - Winning bids
  - Country
  - Year

## 🔍 Exploratory Data Analysis (EDA)

- Cleaned unnecessary columns and handled missing values.
- Sorted data by players for chronological comparison.
- Visualized:
  - Player base price changes over years.
  - Team-wise total base price and bid spending per year.
  - Comparison of **base price vs. winning bid** for players and teams.
  - Country-wise total earnings.

> 📊 Tools used: `pandas`, `matplotlib`, `seaborn`

## 🔧 Feature Engineering

- Encoded categorical features like `Country` and `Team` using `OrdinalEncoder` and `LabelEncoder`.
- Created feature matrix `X` and target variables for:
  - **Regression**: Predicting `Winning bid`
  - **Classification**: Predicting `Team`

## 🤖 Machine Learning Models

### 🎯 Regression (Winning Bid Prediction)
- Model: `RandomForestRegressor`
- Train-test split based on year (< 2022 for train, ≥ 2022 for test)
- Performance metric: `Mean Absolute Percentage Error (MAPE)`

### 🏷️ Classification (Team Prediction)
- Model: `LinearRegression` (used for classification context)
- Target: Encoded team labels
- Metric: `MAPE` between predicted and actual team codes

## 📈 Results

| Task           | Model                 | Metric | Error Rate |
|----------------|-----------------------|--------|------------|
| Winning Bid    | Random Forest         | MAPE   | ~`<insert value>` |
| Team Prediction| Linear Regression     | MAPE   | ~`<insert value>` |

*(Replace placeholder values above after running the notebook)*

## 🚀 How to Run

### 🔧 Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/IPL-Auction-Analysis.git
   cd IPL-Auction-Analysis