# rossmann-sales-forecasting-attention
Time-series forecasting for retail sales using classical statistical models (Prophet) and Deep Learning (LSTM with Attention) to predict daily revenue across 1,115 stores.

# Rossmann Store Sales Forecasting

This project focuses on predicting the daily sales of 1,115 Rossmann drugstores across Europe using advanced time-series forecasting techniques.

## Project Scope
Predicting retail sales is complex due to various external factors. This project explores a progression of models to identify the most effective way to handle seasonality, promotions, and competition.

### Key Drivers Analyzed
* **Promotions:** Impact of active promotional campaigns (Promo and Promo2).
* **Seasonality:** Weekly trends and school/state holiday effects.
* **Competition:** Distance to the nearest competitor and competitor opening dates.

## Modeling Approach
The project implements four distinct modeling strategies:
1.  **Baseline:** A strong Seasonal-Naive model.
2.  **Classical Time-Series:** **Facebook Prophet** for trend and seasonality decomposition.
3.  **Deep Learning (Vanilla):** Standard LSTM model to capture temporal dependencies.
4.  **Deep Learning (Advanced):** **LSTM with Attention Mechanism**.

## Performance Results
The **Attention-based LSTM** significantly outperformed other models:
* **Accuracy:** ~86% average accuracy.
* **Error Rate:** 14.1% Mean Absolute Percentage Error (MAPE).
* **Key Insight:** The attention mechanism allows the model to selectively focus on relevant historical steps (e.g., the same day in the previous week or specific promotional windows), leading to a 66% improvement over the vanilla LSTM.

## Dataset
* **Source:** Rossmann Store Sales dataset (Kaggle).
* **Size:** Over 1 million daily observations across 1,115 unique stores.

## Installation
1.  **Environment Setup:**
    ```bash
    conda create -n rossmann-sales python=3.9
    conda activate rossmann-sales
    ```
2.  **Install Requirements:**
    ```bash
    pip install pandas numpy matplotlib seaborn prophet tensorflow scikit-learn statsmodels
    ```
3.  **Data:** Ensure `train.csv` and `store.csv` are in the project root directory before running the `Project_2.ipynb` notebook.
