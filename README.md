# Imperial Fintec Hackathon Property App - Investate

# House Price Trend Model for Investate

# Overview:
- This repository contains the machine learning module developed as part of the Investate Smart Property Investment System.
The purpose of this model is to categorise monthly price trends (up or down) in the UK housing market based on historical transaction data.

- It integrates cleaned data from the UK Price Paid Dataset and produces both analytical insights and trend forecasts, which can later be connected to the Investate App’s property analytics dashboard.

# Key Objectives:

- Build a predictive categorise model for monthly housing market trend (Up/Down).
- Support postcode level and regional trend visualization.
- Provide an interpretable foundation for property investment recommendations.

# Tech Stack:

Python 3.11

Pandas, NumPy, scikit-learn

Matplotlib / Seaborn for visualization

Jupyter Notebook for experimentation and documentation


# Workflow

Data Preprocessing

Clean monthly transaction data.

Aggregate by YearMonth and PostcodePrefix.

Feature Engineering

Add average price, % month change, property type, and volume metrics.

Encoding

One-hot encode categorical features with frequency filtering.

Model Training

Logistic Regression (SAGA), balanced class weights.

Fit on training months, predict on test months.

Evaluation & Visualization

Output accuracy, F1, AUC.

Draw confusion matrix and ROC curve.

# Usage Example
1. Train the pipeline

pipe.fit(X_train, y_train)

3. Predict on new data (e.g., upcoming month)

pred = pipe.predict(X_new)

4. Get probability of upward trend
   
prob = pipe.predict_proba(X_new)[:, 1]

### Repository Structure
```
Investate-HousePriceTrendModel/
├── HousePriceTrendModel.ipynb
├── data/
├── results/
└── README.md                   
```
