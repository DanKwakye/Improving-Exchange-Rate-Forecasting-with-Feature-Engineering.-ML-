# Improving-Exchange-Rate-Forecasting-with-Feature-Engineering.-ML-

Project Title: Enhancing Exchange Rate Forecasting through Feature Engineering and Machine Learning

1. Introduction
This project focused on predicting Ghana's Inter-Bank Exchange Rates for three major foreign currencies — USD, GBP, and EURO — using historical macroeconomic indicators. With increasing volatility in exchange markets, accurate forecasting is essential for policymakers, importers/exporters, and financial institutions. The goal was to improve predictive accuracy using machine learning, particularly the XGBoost regression model, and evaluate the impact of feature engineering on model performance.

2. Objectives
Build a multi-output regression model to forecast end-period exchange rates.

Compare the performance of models trained on raw features versus engineered features.

Highlight the role of feature engineering and feature selection in enhancing model accuracy.

3. Data Overview
Source: Bank of Ghana and related macroeconomic data.

Time Frame: Monthly data, 2000–2025.

Targets:

Inter-Bank Exchange Rate - End Period (GHC/EURO)

Inter-Bank Exchange Rate - End Period (GHC/GBP)

Inter-Bank Exchange Rate - End Period (GHC/US$)

Features: Included exchange rates (monthly average and end period), economic indicators, and lagged variables.

4. Methodology
Baseline Model
Algorithm: XGBoost Regressor with default tuning.

Input: Raw features (no engineered variables).

Output: Multi-output regression across the three currencies.

Evaluation: MAE (Mean Absolute Error) and RMSE (Root Mean Squared Error).

Feature Engineering Phase
Lag Features: Previous month's values.

Moving Averages: 3, 6, and 12-month averages.

Feature Selection: Used SelectKBest and f_regression to select the top 15 features per target variable.

Model Retraining
Trained a new XGBoost model on the selected engineered features.

Used identical test data (years 2024–2025) for performance comparison.

5. Results

Target	MAE (Raw)	RMSE (Raw)	MAE (Engineered)	RMSE (Engineered)
GHC/EURO	4.1610	5.5622	2.2804	3.6304
GHC/GBP	4.7603	6.3518	2.7411	3.9883
GHC/US$	3.9713	5.1047	2.3455	3.3719
✅ Performance Improvement:

MAE reduced by up to 44%

RMSE reduced by up to 40%

6. Key Takeaways
Feature engineering had a substantial impact on predictive performance.

The engineered model consistently outperformed the baseline across all three targets.

Including time-lagged and rolling average features captured important temporal patterns missed by raw data.

7. Tools & Technologies
Language: Python

Libraries: Pandas, Scikit-learn, XGBoost, Matplotlib

Techniques: Time series lagging, moving averages, SelectKBest, MultiOutput Regression

8. Conclusion
This project demonstrates the critical role of feature engineering in machine learning pipelines. While XGBoost is a powerful model, its full potential is realized only when combined with thoughtful feature preparation. The approach led to significant improvements in forecasting accuracy, making it a robust solution for economic forecasting tasks.

9. Future Recommendations
Incorporate external variables like global commodity prices or inflation indices.

Experiment with neural network architectures like LSTM for sequential modeling.

Deploy the model in Power BI or a web dashboard for real-time insights.
