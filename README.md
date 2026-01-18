
# 🌦️ Weather Time Series Forecasting  
**ARIMA vs Prophet vs LSTM vs GRU**

This repository presents a **comparative study of time series forecasting models** applied to **daily weather temperature prediction**.  
The project focuses on evaluating **classical statistical models** against **deep learning approaches** under the same experimental setup.

The work is intentionally kept **simple, reproducible, and Colab-friendly**, making it suitable for academic projects, self-study, and internship applications.

---

## 🎯 Project Objective

Forecast **daily minimum temperature** and compare the following models:

- **ARIMA** – classical linear time series model  
- **Prophet** – additive model with trend and seasonality  
- **LSTM** – recurrent neural network for long-term dependencies  
- **GRU** – lightweight gated recurrent neural network  

All models are evaluated using **Mean Absolute Error (MAE)** on a held-out test set.

---

## 📊 Dataset

**Daily Minimum Temperatures Dataset**

- Location: Melbourne, Australia  
- Period: 1981 – 1990  
- Frequency: Daily  
- Observations: 3,650  
- Missing values: None  

Raw CSV:  
[https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv](https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv)

---

## 📂 Repository Structure

```
.
├── weather_forecasting_comparison.ipynb   # Main notebook
└── README.md                              # Project documentation
```

---

## ⚙️ Environment & Requirements

Designed to run on **Google Colab**.

Install dependencies:
```bash
pip install prophet statsmodels tensorflow
```

Main libraries:

* pandas, numpy, matplotlib  
* scikit-learn  
* statsmodels  
* prophet  
* tensorflow / keras  

---

## 🧠 Methodology

### Data Preparation

* Date parsing and indexing  
* Strict respect of temporal causality (no shuffling)  
* Train/test split:  
  * Training set: all data except last 365 days  
  * Test set: last 365 days  

### Models

* ARIMA for linear trend and autocorrelation modeling  
* Prophet for seasonality-aware forecasting  
* LSTM and GRU for non-linear temporal dependency modeling  

### Evaluation

* Metric: **Mean Absolute Error (MAE)**  
* Same evaluation protocol for all models  

---

## 📈 Results

| Model   | MAE  |
| ------- | ---- |
| ARIMA   | 3.32 |
| Prophet | 1.94 |
| LSTM    | 1.92 |
| GRU     | 1.81 |

GRU achieves the best performance, followed closely by LSTM, indicating the benefit of recurrent neural networks for capturing non-linear temporal patterns.

---

## 🧾 Conclusion

This project highlights the trade-off between:

* **Interpretability and simplicity** (ARIMA, Prophet)  
* **Model expressiveness and performance** (LSTM, GRU)  

While classical models remain strong baselines, deep learning approaches provide improved accuracy for weather time series forecasting.

---

## ▶️ How to Run

1. Open `weather_forecasting_comparison.ipynb` in **Google Colab**  
2. Run all cells sequentially  
3. Optionally modify:  
   * Forecast horizon  
   * Sliding window size  
   * Number of training epochs  

---

## 🔧 Possible Extensions

* Multivariate forecasting (humidity, wind speed, pressure)  
* Longer forecasting horizons  
* Transformer or state-space models  
* Hyperparameter tuning  

---

## 👤 Author

Time series forecasting comparison project for academic and applied machine learning use cases.

---

### 📌 GitHub Repository Description (short)

```text
Weather time series forecasting project comparing ARIMA, Prophet, LSTM, and GRU on daily temperature data, with time-aware evaluation and MAE-based comparison.
```
