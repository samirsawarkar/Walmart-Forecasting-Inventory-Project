End-to-End Demand Forecasting & Inventory Optimization System (SQL + Python)
A Multi-Store Retail Supply Chain Analytics Project

This project builds an end-to-end analytics system that forecasts demand, calculates safety stock, generates reorder points, and identifies understock/overstock conditions for 45 Walmart stores using SQL + Python.

The goal is to simulate a real supply chain analyst workflow used in companies like Amazon, Flipkart, Walmart, Target, and BigBasket.

🚀 Project Overview

Retail supply chains rely on accurate demand forecasting and optimized inventory planning to minimize stockouts, reduce overstocking, and cut costs.

This project performs:

Time-series demand forecasting

Safety stock estimation

Reorder point (ROP) calculations

Inventory health classification

Recommended order quantities

Multi-model performance comparison

Insights and actionable recommendations

Using historical Walmart sales + macroeconomic drivers, the system produces 12-week demand forecasts and a full inventory optimization pipeline.

📊 Dataset

Source:
https://www.kaggle.com/datasets/yasserh/walmart-dataset

Columns Used:

Store

Date

Weekly_Sales

Holiday_Flag

Temperature

Fuel_Price

CPI

Unemployment

🧠 Key Features
✔ Forecasting Models

SARIMAX

RandomForestRegressor

XGBoost

Prophet

Naive Baseline

Best Model: SARIMAX

RMSE: 59,828

MAE: 48,653

✔ Inventory Modeling

The project computes:

Demand During Lead Time

Safety Stock

Reorder Point (ROP)

Current Stock (Assumed)

Overstock/Understock Status

Recommended Order Quantity

All 45 stores were flagged as Understock, with actionable ordering quantities.

🏗 Project Architecture
project/
│── data/
│── notebooks/
│   └── retail_inventory_optimization.ipynb
│── src/
│   ├── forecasting.py
│   ├── inventory_calculations.py
│   ├── evaluation.py
│   └── eda.py
│── README.md

📈 Major Results
1️⃣ Best Forecasting Model: SARIMAX

Lowest RMSE

Handled seasonal patterns well

More stable than ML models

2️⃣ Inventory Insights

All 45 stores require replenishment.

Safety stock ranges from 57,603 to 619,231 units.

Reorder Points (ROP) vary between 0.7M to 5M units.

Recommended order quantities reflect individual store demand + buffer.

3️⃣ Peak-Demand Insights

Slight demand increase during late December.

Forecast across 12 weeks is stable: 1.04M → 1.08M avg weekly sales.

4️⃣ Cost & Risk Reduction Opportunities

Reduced stockouts → prevents lost revenue

Lower expedited shipping cost

Improved order planning

Balanced safety stock → lower working capital

Better supplier coordination via ROP triggers

🧩 Inventory Health Example
Store	ROP	Current Stock	Status	Recommended Order
1	3.57M	2.40M	Understock	17.17M
4	5.01M	3.29M	Understock	23.65M
45	1.79M	1.12M	Understock	8.18M
📝 Final Conclusion

SARIMAX outperforms all other models, offering the highest accuracy for multi-store retail forecasting.
Combined with safety stock + ROP modeling, the system delivers a complete supply chain decision framework capable of reducing stockouts, lowering operational costs, and improving retail inventory efficiency.

This project represents a real-world supply chain analytics workflow suitable for enterprise-level inventory planning.

🔧 Tech Stack

Python

SQL (optional future extension)

Pandas

Statsmodels

XGBoost

Scikit-Learn

Matplotlib / Seaborn
