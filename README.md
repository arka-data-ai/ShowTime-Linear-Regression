
---

# 📺 ShowTime OTT – First-Day Viewership Analysis

This project analyzes what drives **first-day content viewership** on the ShowTime OTT platform. Using **Linear Regression**, we identify the strongest predictors and build a model to forecast performance for future releases.

---

## 🎯 1. Project Objective

The goal is to understand:

* 📌 Why some titles get higher first-day views
* 📌 Which factors (trailer views, visitors, ads, seasons, days) affect performance
* 📌 How to build a regression model that predicts views
* 📌 What business actions can improve launch outcomes

---

## 📂 2. Dataset Overview

The dataset contains 1,000 content titles with numeric and categorical features.

### 🔢 Numeric Features

* **views_content** → First-day views (target)
* **views_trailer** → Trailer watch count
* **visitors** → Weekly platform visitors
* **ad_impressions** → Number of ad exposures
* **major_sports_event** → 0/1 flag for sports event clash

### 🔤 Categorical Features

* **genre**
* **dayofweek**
* **season**

---

## 🔍 3. Exploratory Data Analysis (EDA)

### 📊 Univariate Analysis

* Histograms and boxplots reveal data distribution.
* Outliers identified but kept (represent genuine high performers).

### 🔗 Bivariate Analysis

* Scatterplots show strong positive relationships:

  * Trailer views → First-day views
  * Platform visitors → First-day views

* Bar charts analyze:

  * Genre vs average views
  * Day of week vs average views
  * Season vs average views

### ⭐ Key EDA Insights

* 🎬 Trailer views are the top driver.
* 👥 More weekly visitors = higher views.
* 🏆 Major sports events reduce performance.
* 📅 Weekends and summer releases perform better.

---

## 🧹 4. Data Cleaning

Performed before modeling:

* No missing values
* No duplicates
* Verified data types
* Outliers detected but retained

Clean data ensures reliable model output.

---

## 🛠️ 5. Feature Engineering

To prepare data for regression:

* One-hot encoded **genre**, **dayofweek**, and **season**
* Dropped one dummy per category (avoid multicollinearity)
* Ensured all variables were numeric

---

## 🧪 6. Model Preparation

* Data split into **70% Training** + **30% Testing**
* Added constant term for intercept
* Chosen model: **Linear Regression (OLS – Ordinary Least Squares)**

---

## 📈 7. Linear Regression Model

The OLS model identifies the impact of each predictor.

### 📘 Model Findings

* 🎬 **views_trailer** → Strongest positive impact
* 👥 **visitors** → High positive influence
* 📣 **ad_impressions** → Moderate positive effect
* 🏆 **major_sports_event** → Strong negative impact
* 📅 Some **days** and **seasons** significantly affect viewership

---

## 🧪 8. Regression Assumption Checks

All major regression assumptions were validated:

* ✔ Linearity
* ✔ Multicollinearity (VIF acceptable)
* ✔ Normality of residuals
* ✔ Homoscedasticity

The model is statistically reliable.

---

## 📊 9. Model Evaluation

Evaluated on the **test set (30%)**.

### 🔧 Metrics:

* **R²:** ~0.75–0.78
* **MAE, MSE, RMSE:** Within acceptable ranges

The model performs well in predicting first-day views.

---

## 💡 10. Business Insights & Recommendations

### Key Insights

1. 🎬 **Trailer views are the strongest driver**
2. 🏆 **Avoid releasing content during major sports events**
3. 👥 **Higher platform visitors lead to more views**
4. 📅 **Weekends and summer seasons perform better**
5. 📣 **Ad impressions boost visibility** (but less than trailers)

### Recommended Actions

* Increase trailer promotions before big releases
* Schedule important releases on weekends/summer
* Boost platform visitors with notifications and campaigns
* Avoid release clashes with major sports events


---

