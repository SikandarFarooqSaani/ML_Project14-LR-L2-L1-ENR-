# 🏠 Boston House Price Prediction

This project predicts **house prices** using the classic **Boston Housing dataset**.  
The aim was to implement different regression models (Linear, Ridge, Lasso, ElasticNet, SGDRegressor), compare their performance, and understand the effect of regularization.

---

## 🛠️ Libraries Used
- Pandas  
- Numpy  
- Scikit-Learn (`LinearRegression`, `Ridge`, `Lasso`, `ElasticNet`, `SGDRegressor`, `train_test_split`, `r2_score`)  
- Statsmodels (for statistical feature selection)  

---

## 📌 Project Steps

### 1. Dataset
- Dataset: **Boston Housing dataset** (attached in project).  
- Preprocessing:
  - Dropped unnecessary columns.  
  - No null or duplicate values → dataset was clean.  
- Defined **X (features)** and **y (target)**.  
- Train-test split with **80:20** ratio.  

---

### 2. Model Training & Results

#### ✅ Linear Regression
- **R² Score:** `0.7789`  

---

#### ✅ Ridge Regression
- Parameters: `alpha = 0.1`  
- **R² Score:** `0.7782`  

---

#### ✅ Lasso Regression
- Parameters: `alpha = 0.2`  
- **R² Score:** `0.7629`  

---

#### ✅ Elastic Net Regression
- Parameters: `alpha = 0.001`, `l1_ratio = 0.8`  
- **R² Score:** `0.7782`  

---

#### ✅ Feature Selection (Statsmodels)
- Used `statsmodels.api` to remove features with **p-value > 0.05**.  
- After dropping unnecessary columns:  
  - Linear Regression → `0.7789`  
  - Ridge Regression → `0.7782`  
  - Lasso Regression → `0.76`  
  - Elastic Net → `0.7782`  

---

## 📊 Observations
- **Linear Regression** gave the best performance (`0.7789`).  
- **Ridge** and **Elastic Net** performed nearly the same (`0.7782`).  
- **Lasso** performed worse (`0.7629`) since it penalized more aggressively and removed some coefficients.  
- Feature selection using **p-values** did not significantly change performance → dataset is already well-structured.  
- Overall, **regularization did not provide major gains**, but it confirmed model stability and feature importance.  

---

## 🚀 Next Steps
- Try **cross-validation** to confirm results.  
- Tune hyperparameters (`alpha`, `l1_ratio`) with **GridSearchCV**.  
- Apply on a larger, modern housing dataset (like **California Housing**).  

---

## 📂 File Structure
