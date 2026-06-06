# Stochastic Interest Rate Modelling and Prediction 📈
**Cox-Ingersoll-Ross (CIR) Model: Implementation, Calibration & Extension**

*Finance Club, IIT Roorkee — Open Projects 2026* **Author:** Aditya Kumar Pandit

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13pUf_5r9UqxiSyT0ca9rNzzH2TBXZMV9?usp=sharing)
[![GitHub Notebook](https://img.shields.io/badge/View-Notebook_on_GitHub-blue?logo=github)](https://github.com/droid-adi/-Stochastic-Interest-Rate-Modelling-and-Prediction/blob/main/Stochastic_Interest_Rate_Modelling_and_Prediction.ipynb)

---

## 📖 Overview
Interest rates are the fundamental building blocks of the global financial system. They dictate the pricing of bonds, the valuation of derivatives, and institutional risk management strategies. 

This project dives deep into short-rate modelling by implementing, calibrating, and extending the **Cox-Ingersoll-Ross (CIR)** model using real historical zero-coupon bond yield data. The primary objective is to evaluate how stochastic short-rate models behave when confronted with noisy historical yield data and to reconstruct an entire yield curve using only a single observable input (the 3-Month rate).

**Target Metric:** Achieve an out-of-sample $R^2$ score greater than **0.85** when reconstructing the full yield curve from the 3M rate.

## 🚀 Project Workflow
The pipeline is structured into five core stages:

| Stage | Description |
|-------|-------------|
| **A** | **Data Engineering & Preprocessing** - Missing value imputation, outlier detection (Z-score), and positivity enforcement on yield data. |
| **B** | **Base CIR Model: Implementation & OLS Calibration** - Modelling the mean-reverting square-root diffusion process. |
| **C** | **Prediction Challenge** - Constructing the entire yield curve strictly from the 3-Month rate. |
| **D** | **Extension** - Enhancing the model to **CIR++** with a Static λ Shift to improve deterministic fitting. |
| **E** | **Critical Analysis & Conclusions** - Evaluating model performance, analyzing limitations, and discussing practical market dynamics. |

## 📊 Dataset
The analysis utilizes daily zero-coupon bond yields across multiple maturity horizons:
* **Training Set (2016-2024):** 3M, 6M, 9M, 1Y, 2Y, 5Y, 10Y, 20Y, 30Y
* **Test Set (2024-2026):** 3M, 6M, 9M, 1Y, 2Y (Yield curve construction relies strictly on the 3M input).

## 💻 Tech Stack & Dependencies
This project is built purely in Python. The notebook requires the following core libraries:
* `numpy` & `pandas` (Data Manipulation)
* `scipy` (Optimization: OLS Calibration, Differential Evolution, Cubic Splines)
* `matplotlib` (Visualization)

## 🛠️ Usage
1. Clone this repository:
   ```bash
   git clone [https://github.com/droid-adi/-Stochastic-Interest-Rate-Modelling-and-Prediction.git](https://github.com/droid-adi/-Stochastic-Interest-Rate-Modelling-and-Prediction.git)
