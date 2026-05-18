# Maize_crop_yield_prediction_punjab_pakistan
This project focuses on predicting Maize Yield across 35 districts of Punjab, Pakistan using Machine Learning techniques and 45 years of historical data (1981–2024). The model uses meteorological, soil, and agronomical features to predict crop yield in kg/acre.

# Project Overview

The objective of this project is to develop an accurate Machine Learning model capable of predicting maize yield using environmental and soil-related factors. The project aims to support agricultural planning, improve crop management, and assist in future yield estimation.

# Dataset Description

The dataset contains:

Meteorological Features
Monthly Temperature
Monthly Precipitation
Relative Humidity
Soil Features
Nitrogen
Soil Organic Carbon (SOC)
Soil pH
Other Features
District
Year
Crop
Target Variable
Maize Yield (kg/acre)
# Data Sources
Pakistan Bureau of Statistics
Punjab Agriculture Department
NASA POWER Data
ISRIC SoilGrids
# Data Preprocessing

The following preprocessing steps were applied:

Outlier handling using the 99th Percentile Method
Creation of Total Precipitation feature
Removal of highly correlated humidity features
One-Hot Encoding of categorical columns
Addition of a yield-zero flag feature
Train/Test split using train_test_split
# Machine Learning Models

The following algorithms were implemented and compared:

Algorithm	R² Score	MAE
Decision Tree	0.8490	244.25
Random Forest	0.9119	199.83
Gradient Boosting	0.9221	183.30
# Best Model

The Gradient Boosting Regressor performed best with:

n_estimators = 800
max_depth = 10
learning_rate = 0.01
# Model Evaluation

The model achieved:

R² Score: 0.9221
MAE: 183.30

Overfitting was checked by comparing training and testing errors using:

staged_predict() function of Gradient Boosting Regressor

The results showed good generalization with closely aligned training and testing error curves.

# Model Interpretation

SHAP Analysis revealed the most influential features:

Soil Features
Germination Temperature
Total Precipitation

The interpretation highlights the importance of sowing time, rainfall, and soil quality for maize production.

# Dashboard Result Example
# Input
District: Okara
Year: 2023
# Output
Real Yield: 3673 kg/acre
Predicted Yield: 3615 kg/acre
# Technologies Used
Python
Pandas
NumPy
Scikit-learn
Matplotlib
SHAP
# Future Improvements
Deep Learning implementation
Satellite imagery integration
Real-time weather forecasting
Web deployment for farmer access
# Author

Developed by Muhammad Zeeshan
BS Computer Science | Machine Learning Enthusiast
