# Machine Learning Coursework - COMP0214

## Overview

This coursework applies machine learning techniques to two real-world problems: retail fuel price forecasting and indoor localization using WiFi signals.

## Project Structure

### Question 1: Fuel Price Forecasting

**Objective:** Predict next-day retail fuel prices for various fuel types across service stations in New South Wales (2016-2025).

**Approach:**
- Data cleaning and aggregation (98,925 → 16,135 daily records)
- Feature engineering: 7-day lagged prices, rolling statistics, temporal features
- Model: Random Forest Regressor (100 trees, max_depth=15)
- Performance: MAE = 2.61 cents/L, MAPE = 1.33%

**Files:**
- `Q1.ipynb`: Complete implementation with data cleaning, visualization, model training, and evaluation
- `data/fuelPrice_NSW.csv`: Raw fuel price dataset

### Question 2: Indoor Localization

**Objective:** Predict X, Y coordinates of a robot based on RSSI (Received Signal Strength Indicator) measurements from WiFi access points.

**Approach:**
- Baseline: Multi-linear regression (validation MSE = 19.71)
- Improved: Neural Network with 438,338 parameters (validation MSE = 7.35, 62.7% improvement)
- Feature analysis: Clustering and dimensionality reduction (PCA) to visualize learned representations

**Performance Metrics:**
- Mean Euclidean Error: 3.04m
- Median Error: 2.43m
- Mean Percentage Error: 6.53%

**Files:**
- `Q2.ipynb`: Complete implementation including preprocessing, linear regression, neural network, and feature visualization
- `data/Wifi_train_dataset.csv`: Training data with RSSI measurements
- `data/Wifi_test_dataset.csv`: Test data for predictions
- `data/zcabofj.txt`: Final predictions for test set

### Report

`report.tex`: Comprehensive 8-page LaTeX report documenting methodology, results, and analysis for both questions.

## Requirements

- Python 3.x
- pandas, numpy, scikit-learn
- TensorFlow/Keras
- matplotlib, seaborn

## Usage

1. Open Jupyter notebooks (Q1.ipynb, Q2.ipynb)
2. Run cells sequentially from top to bottom
3. Outputs include performance metrics, visualizations, and predictions

## Results Summary

**Question 1:** Random Forest successfully captures weekly fuel price cycles with strong forecasting accuracy (1.33% MAPE).

**Question 2:** Neural Network demonstrates robust indoor localization capabilities with mean error of 3.04m, suitable for practical positioning applications.

## Author

Me
