# Retail Supply Chain Analytics: Time Series Demand Forecasting

## Executive Summary
In the retail sector, inventory mismanagement is a multi-million-pound problem. Overstocking ties up working capital and leads to discounted liquidations, while stockouts result in lost revenue and damaged customer loyalty. 

This project develops a machine learning-based Time Series Forecasting model. By ingesting historical daily sales data, the algorithm learns seasonal trends and consumer purchasing patterns to accurately forecast future inventory demand.

**Commercial Objective:** Equip supply chain and procurement teams with a highly accurate 90-day inventory demand forecast, enabling data-driven purchasing decisions that minimise warehouse holding costs and prevent out-of-stock scenarios.

## Technical Stack
* **Language:** Python
* **Machine Learning:** Scikit-Learn (Gradient Boosting Regressor)
* **Time Series Processing:** Pandas (Date-time manipulation, Lag Features, Rolling Windows)
* **Data Visualisation:** Matplotlib, Seaborn

## Core Methodology
1. **Transactional Data Simulation:** Dynamically generates three years of daily sales data for a flagship retail product, mathematically injecting real-world variance such as weekly seasonality (weekend spikes) and annual macro-seasonality (summer slumps and winter holiday peaks).
2. **Time-Based Feature Engineering:** Transforms raw date columns into actionable machine learning features. This includes extracting date parts (Day of Week, Month), generating Autoregressive Lag Features (e.g., sales exactly 7 days ago), and calculating Rolling Averages to smooth out daily noise.
3. **Sequential Predictive Modelling:** Unlike standard machine learning, time series data cannot be randomly split. The model is trained sequentially on the first 2.5 years of data and evaluated on a strict 90-day holdout period using a **Gradient Boosting Regressor**.
4. **Commercial Visualisation:** Outputs a professional forecasting dashboard overlaying the algorithmic predictions against actual historical sales, proving the model's ability to anticipate demand spikes.
