# Price Elasticity Modelling Using PySpark

## Overview

This project focuses on **Price Elasticity Modelling (PEM)** to understand how changes in product prices affect consumer demand. By leveraging PySpark, we analyze a dataset of shoe sales to build a model that predicts the optimal price points for maximizing revenue. The project involves data preprocessing, exploratory data analysis, feature engineering, model training, and price optimization.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Goals](#project-goals)
3. [Dataset Description](#dataset-description)
4. [Methods](#methods)
   - [Data Preprocessing](#data-preprocessing)
   - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - [Feature Engineering](#feature-engineering)
   - [Modeling](#modeling)
   - [Price Optimization](#price-optimization)
5. [Results](#results)
6. [Challenges](#challenges)
7. [Conclusion](#conclusion)

---

## Introduction

Price elasticity measures how sensitive consumer demand is to changes in price. Understanding this relationship is crucial for businesses to optimize pricing strategies and maximize revenue. This project uses **PySpark** to analyze a dataset of shoe sales, build predictive models, and determine the optimal price points for various products.

The key objectives of the project are:
- **Quantify price elasticity** for different products.
- **Predict demand** based on price changes.
- **Optimize prices** to maximize revenue while maintaining customer satisfaction.

---

## Project Goals

- **Understand Price Elasticity:** Classify products into elastic, inelastic, and unitary elasticity categories.
- **Predict Demand:** Build models to predict how changes in price affect the quantity demanded.
- **Optimize Prices:** Use optimization techniques to determine the best price points for maximizing revenue.
- **Provide Actionable Insights:** Help businesses make data-driven pricing decisions.

---

## Dataset Description

The dataset consists of shoe sales data from multiple manufacturers, including:
- **Product Information:** Price, manufacturer, product category, and other attributes.
- **Sales Data:** Quantity sold, date of sale, and promotional details.
- **Competitor Data:** Information on competitor prices and market share.

Key features:
- **Price:** The selling price of the product.
- **Quantity:** The number of units sold.
- **Promotions:** Discounts or coupons applied to the product.
- **Competitor Prices:** Prices of similar products from competitors.

---

## Methods

### Data Preprocessing

- **Handling Missing Values:** Impute missing data using appropriate strategies.
- **Outlier Detection:** Identify and handle outliers in the dataset.
- **Categorical Encoding:** Convert categorical variables into numerical formats using one-hot encoding.
- **Time-Based Splitting:** Split the data chronologically to maintain the temporal nature of sales data.

### Exploratory Data Analysis (EDA)

- **Price Distribution:** Analyze the average price distribution across manufacturers.
- **Price Trends:** Examine how prices have changed over time.
- **Correlation Analysis:** Identify relationships between price, quantity, and promotional metrics.
- **Market Share Analysis:** Study the market share fluctuations for specific manufacturers.

### Feature Engineering

- **Price Positioning Features:** Understand how each product's price fits within its category.
- **Competitor Metrics:** Compare products with competitors in terms of price and market share.
- **Historical Features:** Track price changes and calculate moving averages over different time periods.
- **Promotional Features:** Capture the impact of discounts and promotions on sales.
- **Regional Features:** Account for local market conditions like store density and income levels.

### Modeling

- **Model Selection:** Train three models—Random Forest, Gradient Boosting, and Decision Tree.
- **Hyperparameter Tuning:** Optimize model parameters using cross-validation.
- **Evaluation Metrics:** Use RMSE, MAE, and MAPE to evaluate model performance.

### Price Optimization

- **Price Grid Creation:** Generate a range of price multipliers (0.7 to 1.3 times the current price).
- **Optimization Algorithms:** Use SciPy's L-BFGS-B and SLSQP algorithms to find optimal price points.
- **Constraints:** Apply business constraints like minimum quantity requirements and price bounds.
- **Revenue Maximization:** Iteratively test price scenarios to maximize revenue.

---

## Results

- **Model Performance:** All models (Random Forest, Gradient Boosting, and Decision Tree) performed similarly, with a median percentage error of around 66-68%.
- **Price Optimization:** For specific products, price adjustments led to significant increases in quantity sold and revenue. For example:
  - **Product 54163:** Decreasing the price from $11 to $8 resulted in a 1.6% increase in quantity sold and a 32.1% increase in revenue.
- **Overall Impact:** For a selected range of products, the optimized pricing strategy led to a 4.9% increase in quantity sold over a specific time period.

---

## Challenges

- **Data Quality:** The dataset had inconsistencies, such as limited price variation and incoherent data points.
- **PySpark Limitations:** Lack of built-in optimizers in PySpark required reliance on SciPy for optimization.
- **Infrastructure Constraints:** Memory and connection issues limited the ability to process the full dataset.
- **Feature Interpretation:** Some features, like consumer demographics, had little variation and were difficult to interpret.

---

## Conclusion

This project successfully demonstrates the application of **Price Elasticity Modelling** using PySpark to optimize product pricing. By analyzing price sensitivity, predicting demand, and applying optimization techniques, businesses can make data-driven decisions to maximize revenue while maintaining customer satisfaction. Despite challenges related to data quality and infrastructure, the project provides actionable insights for pricing strategies in the retail industry.

---
