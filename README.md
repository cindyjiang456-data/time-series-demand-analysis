# Time-Series Demand Analysis for Warehouse Inventory

This project analyzes warehouse sales and inventory data using time-series regression to identify demand patterns and evaluate the factors associated with weekly sales.

The analysis focuses on the relationship between sales, inventory levels, price, time trends, and prior-period demand, with the goal of translating historical warehouse data into useful operational insights.

---

## 📌 Project Overview

The project uses one year of daily warehouse-level data from 2025 and transforms it into a structured weekly time-series dataset.

The analysis investigates:

- Historical sales patterns
- Inventory levels
- Average selling price
- Time trends
- Lagged demand

The primary objective is to understand which factors are most strongly associated with weekly sales and how historical demand can inform future inventory and planning decisions.

---

## 🎯 Objectives

- Analyze sales trends using time-series data
- Evaluate the relationship between price, inventory levels, and sales
- Capture temporal dependence using lagged variables
- Build a regression model to explain variations in weekly demand
- Translate statistical results into operational insights

---

## 📂 Dataset

The dataset contains daily warehouse-level observations over one year.

Key variables include:

- **Sales** — total units sold per day
- **Inventory** — daily inventory levels
- **Price** — average selling price

The original dataset was stored in wide format and was transformed into a structured time-series dataset for analysis.

---

## 🛠 Data Processing

The preprocessing workflow included:

- Converting raw wide-format data into long format
- Parsing and formatting date variables
- Aggregating daily observations into weekly data to reduce noise
- Creating a numerical time-trend variable
- Creating lagged weekly sales to capture temporal dependence

### Engineered Features

**Time Trend**

Represents the progression of time across weekly observations.

**Lagged Sales**

Represents sales from the previous period and is used to evaluate whether historical demand helps explain current sales.

---

## 📊 Methodology

A multiple linear regression model was used to analyze weekly sales.

The model can be summarized as:

**Weekly Sales = Price + Inventory + Time Trend + Lagged Sales + Error**

The model was estimated using Python's **statsmodels** library.

The analysis evaluates:

- Model explanatory power
- Statistical significance of predictors
- Temporal dependence in sales
- Relationships between operational variables and demand

---

## 📈 Key Results

- The regression model achieved an **R² of approximately 0.79**, indicating strong explanatory power within the analyzed dataset.
- **Lagged sales were highly significant**, suggesting strong temporal dependence in weekly demand.
- **Price was not statistically significant** as a predictor of weekly sales in this dataset.
- **Inventory levels were not statistically significant** as predictors of weekly sales in this dataset.
- No strong overall time trend was observed during the analyzed period.

---

## 💡 Business Insights

### Historical demand is an important predictor

The strong relationship between lagged sales and current sales suggests that recent demand patterns contain useful information for short-term planning.

Historical sales data may therefore be valuable when developing inventory replenishment or demand-monitoring processes.

### Short-term price and inventory variation showed limited explanatory power

Within this dataset, changes in price and inventory levels were not statistically significant predictors of weekly sales after accounting for other variables in the model.

This does not necessarily imply that price or inventory never influence demand. Rather, their effects were not statistically distinguishable within the available data and model specification.

### Demand showed strong temporal persistence

The significance of lagged sales indicates that weekly demand patterns tend to carry over from one period to the next.

This suggests that incorporating historical demand is important when developing more advanced forecasting models.

---

## ⚠️ Limitations

Several limitations should be considered when interpreting the results:

- Data is aggregated at the warehouse level rather than the individual SKU level
- Discount and promotion variables are not available
- Product-level differences are not captured
- Additional operational factors may influence demand but are not included in the current dataset
- Potential multicollinearity or scaling issues may affect some regression variables
- The analysis covers only one year of observations

These limitations mean that the regression results should be interpreted as exploratory rather than as a complete forecasting system.

---

## 🚀 Future Improvements

Potential extensions of the project include:

- Incorporating SKU-level data
- Adding promotion and discount variables
- Including product categories and lead times
- Expanding the dataset to multiple years
- Performing additional model diagnostics
- Testing alternative feature transformations
- Evaluating ARIMA and other time-series forecasting models
- Comparing regression results with machine-learning approaches
- Developing out-of-sample forecasting and validation procedures

---

## 🧰 Tools & Technologies

- **Python**
- **pandas**
- **NumPy**
- **statsmodels**
- **matplotlib**
- **Jupyter Notebook**

These tools were used for:

- Data cleaning
- Data transformation
- Feature engineering
- Time-series preparation
- Regression modeling
- Statistical interpretation
- Data visualization

---

## 📁 Repository Contents

### Analysis Notebook

[warehouse_time_series_demand_analysis.ipynb](./warehouse_time_series_demand_analysis.ipynb)

Contains the complete analytical workflow, including:

- Data preprocessing
- Weekly aggregation
- Feature engineering
- Exploratory analysis
- Regression modeling
- Statistical interpretation
- Visualization

---

## 💡 Skills Demonstrated

- Python
- pandas
- NumPy
- statsmodels
- Time-Series Analysis
- Regression Analysis
- Statistical Modeling
- Feature Engineering
- Data Cleaning
- Data Transformation
- Data Visualization
- Quantitative Analysis
- Business Analytics
- Inventory Analytics

---

## 📌 Conclusion

This project demonstrates how time-series regression can be applied to warehouse sales and inventory data to identify demand patterns and support operational decision-making.

The analysis found that previous-period sales were the strongest predictor of current weekly demand within the available dataset, highlighting the importance of historical demand when developing inventory planning and forecasting processes.

The project also demonstrates the importance of interpreting statistically insignificant results carefully and identifying opportunities for richer data and more advanced forecasting methods.

---

## 👩‍💻 Author

**Cindy Jiang**

B.S. Mathematics & B.A. Economics  
Pepperdine University

[LinkedIn Profile](https://www.linkedin.com/in/cindy-jiang-a1b7a5272)
