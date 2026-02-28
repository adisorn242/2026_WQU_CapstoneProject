**A Hybrid Explainable Machine Learning Model for Dynamic Asset Allocation: Evidence from the Thai Financial Market**

This repository contains the research code and experimental scripts for developing a hybrid machine learning framework for dynamic asset allocation in the Thai financial market. The study focuses on integrating unsupervised regime detection, supervised ensemble prediction, and explainable AI (XAI) to analyze market dynamics.

_Project Overview_

Traditional portfolio models often struggle with regime shifts in financial markets. This study addresses this by:
1. Identifying market regimes (Bull, Bear, Sideways) using an unsupervised Gaussian Mixture Hidden Markov Model (GM-HMM).
2. Training a supervised ensemble model (Stacking and Voting) to predict future regimes.
3. Integrating predictions into a dynamic Mean-Variance Optimization (MVO) framework.
4. Applying SHAP to provide transparency into the model's decision-making logic.

_Methodology_

The research is structured into four primary phases:

Phase 1: Data Collection & Feature Engineering
- Extraction of weekly SET Index data and top 100 market cap stocks.
- Calculation of logarithmic returns, Open-to-High (OHR), and Open-to-Low (OLR) features.
- Technical indicator engineering (MACD, RSI, MFI, ATR, OBV).

Phase 2: Regime Detection Engine
- Unsupervised Labeling: Using Multivariate GM-HMM to define market states.
- Supervised Prediction: Developing a stacked generalization framework using XGBoost, DNN, Random Forest, SVM, and Logistic Regression.
- Interpretability: Using SHAP to analyze feature contributions.

Phase 3: Portfolio Construction
- Implementation of regime-switching MVO.
- Adaptive risk-aversion coefficients based on predicted market states.
- Weekly rebalancing strategy.

Phase 4: Evaluation
- Backtesting against Benchmarks (Buy-and-Hold SET, Equal Weight, Static MVO).
- Analysis of Sharpe Ratio, Sortino Ratio, and Maximum Drawdown.
- Performance Summary

_Research Environment:_

The research findings are based on the following library versions:

- joblib==1.5.3
- numpy==2.0.2
- tensorflow==2.19.0
- pandas==2.2.2
- yfinance==0.2.66
- cvxpy==1.6.7
- scikit-learn==1.6.1
- requests==2.32.4
- matplotlib==3.10.0
- seaborn==0.13.2
- hmmlearn==0.3.3
- scipy==1.16.3
- statsmodels==0.14.6
- mplfinance==0.12.10b0
- xgboost==3.2.0
- shap==0.50.0
- keras-tuner==1.4.8
- arch==8.0.0


_Authors_

Adisorn Promkaewngarm and Yongli Chen

This project was developed as a Capstone Project for WorldQuant University (WQU).
