# Forecasting Methods: Walmart Retail

## 1. Classical Statistical Models

**Best when data is smaller, interpretable, and seasonal patterns are strong.**

- **ARIMA / SARIMA (AutoRegressive Integrated Moving Average)**
  - Captures trend + seasonality.
  - SARIMA extends ARIMA by handling seasonal cycles (like weekly patterns).
  - *Example:* “Sales today depend on sales yesterday + random noise + weekly seasonality.”

- **Prophet (by Facebook/Meta)**
  - Easy-to-use tool for business forecasting.
  - Handles trend, seasonality, holidays.
  - TPM-friendly (no deep math needed, just specify known holidays/events).
  - *Example:* Walmart can add "Black Friday" as a holiday effect.

- **ETS (Error, Trend, Seasonality)**
  - Similar to Holt-Winters but more flexible in decomposing time series into components.
  - Handles additive or multiplicative seasonality.

---

## 2. Machine Learning Approaches

**Useful when you have many stores/products and want to model external features (weather, promotions, holidays).**

- **Random Forest / XGBoost / Gradient Boosted Trees**
  - Works on tabular features (e.g., day-of-week, holidays, last-7-days sales).
  - Can handle non-linear effects better than ARIMA.
  - Good for demand forecasting across many SKUs.

- **Support Vector Regression (SVR)**
  - Models complex non-linear sales patterns.
  - Works well if you engineer good time-based features.

---

## 3. Deep Learning Models

**Scalable, powerful—used in modern retail demand forecasting.**

- **RNN / LSTM (Recurrent Neural Networks)**
  - Captures long-term dependencies in time series.
  - Useful for highly seasonal + trend-driven sales.
  - *Example:* LSTM can learn both weekly + holiday spikes.

- **Temporal Convolutional Networks (TCN)**
  - Uses convolution instead of recurrence.
  - Often faster and better for multi-step forecasting.

- **Transformers (e.g., Informer, TFT, GPT-like models for time-series)**
  - State-of-the-art for complex forecasting.
  - Handles multi-variate (many features: sales, weather, promotions, traffic).
  - *Example:* Walmart’s global supply chain demand forecasting at scale.

---

## 4. Hybrid / Ensemble Methods

**Combine statistical + ML.**

- *Example:* Use SARIMA for baseline seasonality + XGBoost for residuals (promotion effects).
- Very common in real retail forecasting pipelines.

---

## 5. Cloud AutoML & Managed Solutions

**Since you’re training TPMs who may not code:**

- **Google Vertex AI Forecasting (AutoML Tables for time series)**
- **AWS Forecast**
- **Azure AutoML Forecasting**

> These automatically try multiple models (Prophet, ARIMA, DeepAR, etc.) and pick the best.

---

