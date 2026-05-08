# 🍕 Food Demand Forecasting & Optimization

## 📌 Project Overview
The objective of this project is to accurately forecast the weekly food demand (number of orders) for various meal-center combinations of a food delivery service. Accurate demand forecasting is crucial for:
- **Inventory Management:** Ensuring the right amount of ingredients are in stock.
- **Waste Reduction:** Minimizing food spoilage and reducing costs.
- **Logistics Optimization:** Planning delivery staff and center operations efficiently based on expected volume.

## 📊 Dataset Overview
To perform a comprehensive analysis, we utilized a rich dataset composed of three main files:
- `train.csv`: Historical transactional data including the target variable `num_orders`.
- `meal_info.csv`: Auxiliary data categorizing meals by cuisine and category.
- `fulfilment_center_info.csv`: Information regarding the fulfillment centers (region, city code, center type, and operational area).

## 🔍 Key Exploratory Data Analysis (EDA) Insights
During our collaborative group EDA phase, we identified several critical business insights:
- **High Volatility:** The overall aggregated demand does not follow a smooth, steady trend. Instead, it features extreme and sudden spikes.
- **The Power of Promotions:** Marketing campaigns drastically drive demand. Our analysis showed that during weeks with active email promotions, the average number of orders effectively triples.
- **Price Elasticity:** As expected economically, there is a clear negative correlation between the checkout price and the total number of orders.

## ⚙️ Validation Strategy
To rigorously evaluate our forecasting models and prevent **data leakage** (where a model learns from future events to predict the past), we implemented a strict **Chronological Split** (Time-Based Split):
- **Training Set:** The first 130 weeks of historical data.
- **Validation/Test Set:** The remaining 15 weeks (Weeks 131 to 145).

## 🤖 Modeling & Evaluation
To solve this forecasting problem, each team member developed, tuned, and evaluated distinct time-series models in their individual notebooks. The models explored include:
- **Naïve Forecast** (Baseline)
- **Exponential Smoothing** (Holt-Winters)
- **ARIMA** (AutoRegressive Integrated Moving Average)

**Evaluation Metrics:**
All individual models are objectively compared using:
- **MAE (Mean Absolute Error):** To understand the average magnitude of forecasting errors in real order quantities.
- **RMSE (Root Mean Squared Error):** To heavily penalize large forecasting errors, which is particularly important given the sudden promotional demand spikes identified during our EDA.

## 👥 Contributors
- **Komal** - Repository Setup, Data Preparation, Initial EDA (Trends & Stationarity), and Problem Definition.
- **Badr Kourdad** - Advanced EDA (Marketing Impact), Validation Strategy (Chronological Split), GitHub Documentation, Individual ARIMA Modeling, Notebook Structuring & Professional Markdown Formatting, 
- **Jainil Bhatasana** - Probabilistic Modeling (Gaussian Naïve Bayes), Target Discretization (Binning), and Lead Evaluator for Mean Absolute Error (MAE) Analysis.
- **[name]** - 
