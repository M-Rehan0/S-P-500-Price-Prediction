# S&P 500 Stock Price Prediction and Historical Event Analysis

## Project Overview
This project analyzes the impact of major historical events—specifically the **2008 Financial Crisis** and the **COVID-19 pandemic**—on S&P 500 stock prices using machine learning and big data tools. Developed with 4 other members, the goal is to predict stock prices while accounting for biases introduced by these events, providing insights into how crises influence market behavior.

## Key Features
✔ **Data Analysis**: Examines stock performance metrics (Daily Return, Volume, VWAP, Drawdown, Volatility) across different market conditions  
✔ **Machine Learning**: Uses a Random Forest Regressor to predict stock prices  
✔ **Big Data Processing**: Leverages Spark (PySpark) and SQL for efficient data handling  
✔ **Event-Driven Insights**: Compares model performance with/without crisis data  

## Methodology

### 1. Data Pipeline
- **Data Extraction**: S&P 500 stock data sourced from Kaggle
- **Data Cleaning**:
  - Removed missing values
  - Checked for duplicates
- **Feature Engineering**:
  - One-hot encoded "Ticker" column
  - Split date into year/month/day features

### 2. Model Training
- **Algorithm**: Random Forest Regressor
- **Training Strategy**:
  | Model | Data Included |
  |-------|---------------|
  | 1 | Full dataset (with both crises) |
  | 2 | Excluding 2008 Crisis |
  | 3 | Excluding COVID-19 |
  | 4 | Excluding both crises |
- **Evaluation Metric**: Root Mean Squared Error (RMSE)

### 3. Key Findings

#### 2008 Financial Crisis (2007-2009)
- 📉 **Financial stocks**: AIG (-0.0086 daily return)
- 💹 **Resilient sectors**: Tech (AAPL, AMZN)
- 📈 **Volatility spike**: AIG 0.0747 (vs pre-crisis 0.0072)

#### COVID-19 Pandemic (2020)
- 🚀 **Top performers**: 
  - TSLA (PRR 679.57%) 
  - MRNA (PRR 358.67%)
- ✈️ **Struggling sectors**: 
  - UAL (PRR 42.46%) 
  - CCL (PRR 33.33%)

### 4. Model Performance
- **Best Model**: Full dataset (RMSE: 1.23)
- **Case Studies**:
  - MRNA: +3.43 higher predictions with COVID data
  - UAL: -1.27 lower predictions with COVID data

## Technical Implementation
| Category        | Technologies |
|-----------------|-------------|
| Languages       | Python, SQL |
| Frameworks      | Spark, Scikit-learn |
| Data Processing | ELT Pipeline |
| Key Metrics     | VWAP, Drawdown, PRR |

## Why This Project Matters
✅ Real-world ML application in finance  
✅ Quantifies crisis impacts on markets  
✅ Demonstrates scalable big data solutions  
