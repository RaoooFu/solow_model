# 📈 Final Project: Predicting Economic Growth Using the Solow Model and Machine Learning

**Author:** Rao Fu  
**Date:** June 2025

## 📌 Project Overview

This project combines classical economic theory with modern machine learning techniques to analyze and predict economic growth across countries using the Solow-Swan model framework. The goal is to identify the influence of investment, population growth, and human capital on GDP per capita — and evaluate these drivers across different stages of economic development.

---

## 🎯 Research Question

**What roles do investment, population growth, and human capital play in shaping GDP per capita, and how do these drivers vary across countries at different stages of development?**

---

## 🧠 Theory: Solow Growth Model

The Solow Model posits that:
- **Investment** leads to capital accumulation and boosts GDP per capita.
- **Population Growth** dilutes capital and slows GDP per capita growth.
- **Human Capital (education)** improves productivity and accelerates growth.

---

## 📊 Data Sources

| Variable                  | Source                          | Years         |
|---------------------------|----------------------------------|---------------|
| GDP per Capita            | S&P Global                      | 1990–2055     |
| Investment Share of GDP   | S&P Global                      | 1990–2040     |
| Population Growth Rate    | S&P Global                      | 1990–2055     |
| Avg. Years of Schooling   | Our World in Data               | 1950–2040     |

---

## 🧹 Data Preparation

- Reshaped all datasets to long format
- Merged on `Country` and `Year`
- Scaled numerical features using **Min-Max Scaler**
- Segmented countries into:
  - **Developed** (Netherlands, UK, Australia)
  - **Late Industrializers** (Japan, Singapore)
  - **Developing** (China, Brazil, Argentina, India)

---

## 🧪 Models & Results

### 🔁 Linear Regression
- **All countries**: R² = 0.512  
- **Developed**: R² = 0.512  
- **Late Industrializers**: R² = -0.170  
- **Developing**: R² = 0.63

### 🔍 Coefficient Interpretation (Developing):
- Population Growth → **−1.75**
- Schooling → **+1.35**
- Investment → **−1.38**

### 🌳 Decision Trees & Ensemble Models

| Model             | Developed | Late Ind. | Developing |
|------------------|-----------|-----------|------------|
| Random Forest     | 0.779     | -1.647    | 0.725      |
| Gradient Boosting | 0.719     | -5.314    | 0.448      |
| Adaboost          | 0.774     | 0.653     | 0.653      |

---

## 🔍 Key Insights

- **Education (schooling)** consistently improves economic growth, especially in developing nations.
- **Population growth** tends to negatively correlate with GDP per capita across all segments.
- **Investment** shows mixed influence, especially in developing countries, possibly due to inefficiencies or lag effects.
- Ensemble models **significantly improved accuracy** over basic regression models in most segments.

---

## 💡 Next Steps

- Expand country samples for each segment
- Test time-series forecasting techniques
- Integrate institutional quality or infrastructure variables
- Visualize segmented trends in an interactive dashboard

---

## 📁 Files

- `solow_swann.ipynb`: Main notebook with full analysis and modeling
- `final.pdf`: Final project presentation

---


---
