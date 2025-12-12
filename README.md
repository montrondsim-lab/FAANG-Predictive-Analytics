Project Overview

This project explores whether machine learning models can meaningfully predict the daily direction of stock price movements for major technology companies commonly referred to as FAANG: Facebook Meta, Apple, Amazon, Netflix, and Google.

Using historical stock price data, the analysis focuses on identifying patterns in returns, trends, and volatility and evaluating whether these signals can be used to predict whether a stock’s price will move up or down the following trading day. The project combines exploratory data analysis with predictive modeling and emphasizes interpretability and real world relevance rather than purely optimizing accuracy.

This work was completed as part of the ISOM 835 course at Suffolk University and is intended to demonstrate applied data analytics skills in a financial context.

Business Problem

Financial markets are noisy and highly efficient, making short term price prediction extremely challenging. Despite this, technical indicators such as returns, moving averages, and volatility are widely used by analysts and traders to inform decision making.

The core question of this project is whether these commonly used indicators contain enough information to support short term directional predictions and whether more complex machine learning models provide meaningful improvements over simpler approaches.

Objectives

The objectives of this project are to explore historical stock behavior across FAANG companies, build and evaluate machine learning models that predict next day price direction, compare model performance across firms and algorithms, translate technical results into business relevant insights, and reflect on ethical considerations related to predictive modeling in financial markets.

Dataset

The dataset consists of daily historical stock price data for FAANG companies sourced from Kaggle. Each record includes standard market variables such as open, high, low, close, adjusted close, and trading volume.

From these raw inputs, additional features were engineered including daily returns, short and medium term moving averages, and rolling volatility measures. The prediction target is a binary variable indicating whether the following day’s closing price is higher or lower than the current day.

Methodology

The analysis begins with exploratory data analysis to understand long term trends, volatility regimes, and return distributions. Feature engineering was then applied to capture momentum and risk characteristics commonly referenced in financial analysis.

Two supervised learning models were implemented. Logistic Regression was used as a baseline due to its interpretability and suitability for binary classification. A Random Forest classifier was also tested to evaluate whether a more flexible nonlinear model could capture additional structure in the data.

Models were evaluated using out of sample accuracy and compared across companies to assess consistency and robustness.

Key Findings

Across all FAANG companies, model performance was only modestly better than random guessing. Logistic Regression consistently outperformed Random Forest, suggesting that simpler linear relationships were more stable than complex nonlinear patterns.

Feature importance analysis revealed that daily returns dominated model predictions, while moving averages and volatility contributed little incremental value. This highlights the difficulty of extracting predictive signals from widely available technical indicators in efficient markets.

Business Insights

From a business perspective, the results reinforce the importance of caution when deploying short term predictive models in financial settings. While machine learning can help structure and analyze large datasets, its ability to generate reliable trading signals from basic technical indicators appears limited.

The findings suggest that such models may be better suited for risk monitoring or decision support rather than direct trading execution.

Ethics and Responsible Use

Predictive models in finance carry ethical risks, including overconfidence in model outputs, unintended amplification of market volatility, and unequal access to sophisticated tools. This project emphasizes transparency, interpretability, and acknowledgment of limitations as key principles for responsible deployment.

Models should complement human judgment rather than replace it, particularly in high risk financial decision making.

Repository Structure

The data folder contains the raw historical stock price datasets used in the analysis.
The notebooks folder includes the exploratory data analysis and modeling workflows implemented in Google Colab.
The images folder contains key visualizations used in the analysis and final report.
The reports folder contains the final written project report.

Tools and Libraries

Python was used for all analysis with pandas and numpy for data manipulation, matplotlib and seaborn for visualization, and scikit learn for machine learning. All work was conducted in Google Colab for reproducibility.

Acknowledgments

This project was completed as part of the ISOM 835 course at Suffolk University. Some code generation and debugging assistance was provided by AI tools. All analysis, interpretation, and conclusions are my own.
