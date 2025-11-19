# 📈 Warehouse Sales Forecast

This project aims to **predict monthly sales** using historical warehouse and retail data.  
The model applies several regression-based approaches such as **Lasso**, **Ridge**, **Random Forest**, and **Gradient Boosting** to estimate total sales performance.

---

## 📊 Dataset
The dataset (`Warehouse_and_Retail_Sales.csv`) contains yearly and monthly information on:
- Retail Sales  
- Warehouse Sales  
- Retail Transfers  

These columns are combined into a single metric called **`TOTAL_SALES`**, which serves as the main target variable for analysis and forecasting.

---

## 🧠 Main Steps
1. **Data Preprocessing** – merging columns and converting dates  
2. **Exploratory Data Analysis (EDA)** – identifying sales trends and patterns  
3. **Feature Engineering** – creating lag and rolling window features  
4. **Model Training** – applying various regression models  
5. **Evaluation** – comparing results using MAE, RMSE, and R² metrics  
6. **Visualization** – plotting predicted vs. actual sales values  

---

## 🏆 Results
The **Lasso Regression** model achieved the best performance with:
- **MAE:** ~12,411  
- **R² Score:** 0.868  

---

## 💡 Insights
- Adding lag and rolling window features significantly improved forecast accuracy.  
- The model captures seasonal patterns and overall sales trends effectively.  
- Lasso performed best due to its ability to reduce overfitting and handle correlated features.

---

## 🔮 Future Improvements
- Experiment with advanced models such as **ARIMA**, **Prophet**, or **LSTM** for time-series forecasting.  
- Integrate a **Streamlit dashboard** for interactive visualization.  
- Include external factors (e.g., holidays, promotions, weather) to enhance accuracy.

---
