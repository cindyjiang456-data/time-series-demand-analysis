# 📊 Time-Series Demand Analysis for Warehouse Inventory

## 📌 Project Overview

This project analyzes warehouse sales and inventory data using a time-series regression approach to understand the key drivers of demand. The goal is to identify how operational factors such as pricing and inventory levels influence sales over time, and to capture temporal patterns in demand.

---

## 🎯 Objectives

- Analyze sales trends using time-series data
- Evaluate the impact of price and inventory on demand
- Capture temporal dependence using lagged variables
- Build a regression model to explain variations in sales

---

## 📂 Dataset

The dataset consists of daily warehouse-level data over one year (2025), including:

- **Sales**: Total units sold per day  
- **Inventory**: Daily inventory levels  
- **Price**: Average selling price  

The data was originally in a wide format and was transformed into a structured time-series dataset.

---

## 🛠 Data Processing

Key preprocessing steps included:

- Converting raw wide-format data into long format
- Parsing and formatting date variables
- Aggregating daily data into **weekly observations** to reduce noise
- Creating additional features:
  - **Time trend variable**
  - **Lagged sales variable (Salesₜ₋₁)**

---

## 📊 Methodology

A multiple linear regression model was used to analyze weekly sales:

\[
Sales_t = \beta_0 + \beta_1 Price_t + \beta_2 Inventory_t + \beta_3 Time_t + \beta_4 Sales_{t-1} + \epsilon_t
\]

The model was estimated using Python’s `statsmodels` library.

---

## 📈 Key Results

- **R² ≈ 0.79**, indicating strong explanatory power  
- **Lagged sales (Salesₜ₋₁)** was highly significant, suggesting strong temporal dependence in demand  
- Price and inventory were not statistically significant predictors in this dataset  
- No strong time trend was observed  

---

## 💡 Insights

- Sales exhibit strong persistence over time, meaning past demand is a key predictor of future demand  
- Short-term changes in price and inventory levels may not significantly impact sales  
- Demand patterns appear stable and driven by underlying trends rather than operational fluctuations  

---

## 📉 Limitations

- Data is aggregated at the warehouse level (no SKU-level detail)  
- No discount or promotion variables available  
- Potential multicollinearity or scaling issues in regression variables  

---

## 🚀 Future Improvements

- Incorporate SKU-level data to perform panel data analysis  
- Include additional variables such as promotions, categories, and lead times  
- Apply time-series models such as ARIMA or machine learning approaches  
- Perform feature scaling and model diagnostics  

---

## 🧰 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Statsmodels  
- Matplotlib / Seaborn  

---

## 📌 Conclusion

This project demonstrates how time-series regression can be applied to real-world warehouse data to uncover demand patterns and inform inventory management decisions.

---

## 👤 Author

Cindy Jiang  
B.A. Economics & B.S. Mathematics  
