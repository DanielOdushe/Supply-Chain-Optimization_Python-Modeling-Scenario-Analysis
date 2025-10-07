# Delivery Delay Prediction Project

## 📋 Project Overview
This project focuses on predicting delivery delays in logistics operations using machine learning. By analyzing historical delivery data, we identify key factors that contribute to delays and build predictive models to flag potential late deliveries in advance.

## 🎯 Business Problem
Delivery delays can significantly impact:
- **Customer satisfaction** and brand reputation
- **Operational costs** through re-routing and urgent handling
- **Revenue loss** from canceled orders
- **Supply chain efficiency** through ripple effects

## 📊 Dataset Summary
- **Total Records**: 15,549 orders
- **Features**: 39 variables including customer, product, order, and shipping information
- **Target Variable**: `label` (-1: Late, 0: On-time, 1: Early)
- **Data Quality**: No missing values in any column

### Key Data Categories:
- **Customer Information**: Segment, location, zipcode
- **Order Details**: Payment type, profit, sales amount
- **Product Information**: Category, price, discount rates
- **Shipping Details**: Mode, dates, regions
- **Geographic Data**: Latitude, longitude coordinates

## 🔧 Methodology

### 1. Data Preprocessing & Feature Engineering
- Processed order and shipping dates to calculate **shipping duration**
- Encoded categorical variables (shipping_mode, customer_segment, etc.)
- Created additional features including high-volume customer flags

### 2. Exploratory Data Analysis
- Analyzed distributions of numerical variables (sales, profit, discounts)
- Examined categorical variable frequencies and patterns
- Identified correlations between features and delivery outcomes

### 3. Model Development
Trained and evaluated three machine learning models:
- **XGBoost**
- **Random Forest**
- **Logistic Regression**

## 📈 Model Performance

| Model | Accuracy | F1 Score |
|-------|----------|----------|
| Logistic Regression | 57.75% | 42.32% |
| Random Forest | 57.68% | 51.75% |
| XGBoost | 56.56% | 52.97% |

## 🔍 Key Insights

### Top 5 Most Important Features:
1. **Shipping Mode** (42.8% importance)
2. **Shipping Duration** (2.5% importance)
3. **Product Category ID** (2.1% importance)
4. **Order Profit per Order** (2.0% importance)
5. **Order Item Total Amount** (2.0% importance)

### Critical Findings:
- Shipping mode is the strongest predictor of delivery timeliness
- Geographic factors (latitude/longitude) significantly influence delivery outcomes
- Customer location and order value play moderate roles in delay prediction
- Profit margins and discount rates show measurable impact on delivery performance

## 🚀 Recommendations

### Operational Improvements:
1. **Optimize Shipping Strategies**: Focus on improving performance of shipping modes with high delay rates
2. **Regional Priority Handling**: Flag high-risk geographic areas for expedited processing
3. **Customer Segmentation**: Implement differentiated handling for high-value customer segments
4. **Real-time Monitoring**: Incorporate shipping duration tracking in logistics dashboards
5. **Resource Allocation**: Use predictive insights to pre-allocate resources during peak periods

## 📁 File Structure