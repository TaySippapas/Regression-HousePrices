Ames Housing Price Prediction
Overview

This project investigates house price prediction on the Ames Housing dataset, with an emphasis on structured preprocessing, feature engineering, and systematic model comparison. The objective is to evaluate classical machine learning models and neural networks under a unified experimental setting.

Methods

Missing values are handled using domain-informed strategies, including neighborhood-based imputation, ordinal encoding for quality-related features, and zero-filling where the absence of a feature is meaningful. Categorical variables are processed through a combination of ordinal mappings and one-hot encoding. Feature engineering is applied selectively, including aggregated area features for linear regression models. A range of regressors are evaluated: Linear Regression, SVR, KNN, Random Forest, Gradient Boosting, XGBoost, LightGBM, and a feedforward Neural Network.

Model Selection and Optimization

Among all evaluated models, XGBoost achieved the strongest baseline performance, obtaining a Kaggle public leaderboard score of 0.135 (Log RMSE). Consequently, XGBoost was selected for hyperparameter optimization using Randomized Search, which further improved performance to 0.129, resulting in a Kaggle rank of 1853 out of 6108 submissions as of December 18, 2025.

Evaluation

All models are evaluated using Log RMSE, a standard metric for housing price prediction that reduces skewness in the target distribution and enables fair comparison across models.

Results and Discussion

Tree-based ensemble methods consistently outperform linear models and neural networks on this dataset. In particular, XGBoost and Gradient Boosting demonstrate superior generalization. The neural network exhibits weaker performance, reinforcing the observation that deep learning models often require larger datasets and extensive tuning to compete with ensemble methods on tabular data.