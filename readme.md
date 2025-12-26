# 📈 Market Regime Detection Using Hidden Markov Models

> A data-driven framework for identifying market regimes and improving risk-aware investment decisions using Indian equity market data.

---

## 🔍 Project Overview

Financial markets operate under different **regimes** — periods of growth, stress, or consolidation.  
This project builds a **Hidden Markov Model (HMM)**–based system to detect such regimes in the Indian stock market and analyze their impact on market behavior.

Instead of predicting prices, the focus is on **understanding market structure**, volatility dynamics, and regime persistence.

---

## 🧠 Objectives

- Identify latent market regimes using statistical learning
- Interpret regimes using financial intuition
- Analyze regime-dependent risk and return behavior
- Demonstrate a clean, reproducible data science workflow

---

## 📊 Dataset

- **Source:** Yahoo Finance  
- **Instrument:** NIFTY 50 Index  
- **Frequency:** Daily  
- **Period:** 2010 – Present  

### Engineered Features
- Log Returns  
- Rolling Volatility (20-day)  
- Rolling Mean Return  
- Price-to-Moving-Average Ratio  

---

## 🧩 Methodology

### 1️⃣ Data Preparation
- Cleaned and standardized historical market data
- Removed missing values and engineered rolling features

### 2️⃣ Regime Detection (Core Model)
- Used **Gaussian Hidden Markov Model (HMM)**
- Trained on market behavior features rather than prices
- Identified latent market regimes

### 3️⃣ Regime Interpretation

| Regime | Characteristics | Interpretation |
|------|----------------|----------------|
| 0 | High volatility, negative returns | Stress / Risk-Off |
| 1 | Moderate volatility, flat returns | Sideways |
| 2 | Low volatility, positive returns | Bull / Risk-On |

---

## 📈 Strategy Evaluation

A simple regime-aware strategy was tested:

- **Invested** during Bull & Sideways regimes  
- **Reduced exposure** during Stress regimes  

Performance was compared against a Buy & Hold benchmark using:
- Cumulative returns
- Drawdowns
- Risk-adjusted metrics

---

## 📊 Key Findings

- Market regimes are clearly distinguishable using volatility and trend features  
- Regime-aware strategy reduces drawdowns during stress periods  
- Results are stable under out-of-sample testing  
- Regime behavior aligns with known market events (e.g., 2008, COVID-19)

---


---

## 🧪 Technologies Used

- Python  
- pandas, numpy  
- scikit-learn  
- hmmlearn  
- matplotlib / seaborn  

---

## 📌 Key Takeaways

- Market regimes can be statistically identified using latent variable models  
- Volatility plays a dominant role in regime transitions  
- Regime-aware strategies improve risk management  
- Interpretation and robustness matter more than raw prediction accuracy  

---

## 🚀 Future Enhancements

- Incorporate macroeconomic indicators (VIX, interest rates)
- Extend to multi-asset portfolios
- Apply Bayesian HMMs
- Add transaction cost modeling




