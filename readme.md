# Walmart Sales Forecasting

This project analyzes Walmart’s historical sales data to understand store-level and department-level performance patterns and build forecasting models that predict weekly sales. The dataset includes store metadata, weekly sales records, and additional external features such as holidays, fuel prices, temperature, and CPI. The notebook performs end-to-end data preparation, exploratory data analysis (EDA), visualization, feature engineering, and time-series forecasting using Auto-ARIMA and Exponential Smoothing. The goal is to demonstrate practical skills in data cleaning, merging datasets, time-series modeling, and generating insights from retail data.

## 📁 Dataset

The notebook uses the following datasets (ensure they are in the same folder as the notebook):

- train.csv — weekly sales records  
- stores.csv — store metadata  
- features.csv — external economic and seasonal indicators  
- clean_data.csv — (optional) saved cleaned dataset produced by the notebook

## 📂 Project Structure

.
├── Wamart_Sales_Forecasting.ipynb
├── train.csv
├── stores.csv
├── features.csv
├── clean_data.csv        # created by notebook
└── README.md

## 🔍 Key Steps in the Notebook

### 1. Data Loading & Merging  
All three datasets (train, stores, features) are merged into a unified dataframe for analysis.

### 2. Exploratory Data Analysis  
Includes:
- Distribution of weekly sales  
- Store-wise & department-wise trends  
- Holiday impact analysis  
- Correlation heatmaps  
- Seasonal patterns and weekly cycles  

### 3. Feature Engineering  
- Date conversion into year, month, week  
- Rolling averages for smoothing  
- Handling missing values  
- Removing/keeping relevant columns after merge  

### 4. Time-Series Modeling  
Models implemented in the notebook:
- Auto-ARIMA (pmdarima.auto_arima)  
- Exponential Smoothing (Holt-Winters)  

Both models are fit on training splits and evaluated on test sets with visual prediction comparisons.

## ⚙️ Requirements

You may create a requirements.txt with the following:

numpy
pandas
matplotlib
seaborn
scikit-learn
statsmodels
pmdarima
warnings
jupyter

Install using:

pip install -r requirements.txt

## ▶️ How to Run the Project

1. Clone the repository  
2. Place train.csv, stores.csv, and features.csv in the repo directory  
3. Install dependencies  
4. Launch Jupyter:

jupyter notebook

5. Open Wamart_Sales_Forecasting.ipynb and run all cells sequentially

## 📈 Results Overview

- Auto-ARIMA and Holt-Winters both generate weekly sales forecasts  
- Visual comparisons show model performance for trends and seasonality  
- The analysis highlights how promotions and holidays affect store-level sales  
- This project demonstrates real retail forecasting workflow used in data science jobs

## 🚀 Future Improvements

- Try XGBoost/LightGBM time-series models with lag features  
- Implement Prophet or SARIMAX for complex seasonality  
- Build an interactive Streamlit dashboard  
- Add MAPE/RMSE model comparison table  
- Deploy model as an API for real-time forecasting  

## 📌 Git Commands to Push This Project

git add Wamart_Sales_Forecasting.ipynb README.md
git commit -m "feat: added Walmart Sales Forecasting notebook, EDA, feature engineering, and forecasting models"
git push -u origin main

## 📜 License

Add your preferred license (MIT recommended) if making the project public.
