# 🏠 Chennai House Price Prediction

Predict house prices in **Chennai** using Machine Learning models. This project covers data cleaning, exploratory data analysis (EDA), feature engineering, and regression modeling.

---

## 📌 Project Overview

The goal of this project is to predict the **sales price** of houses in Chennai using historical property data.  
The dataset contains property details like area, bedrooms, bathrooms, building type, and amenities.

**Key Steps:**
1. Data Cleaning & Handling Missing Values
2. Feature Engineering & Encoding
3. Exploratory Data Analysis (EDA)
4. Model Training & Evaluation
5. Feature Selection & Importance

---

## 🗂 Dataset

**Main Columns:**
- `AREA` – House location  
- `INT_SQFT` – Interior area in square feet  
- `N_BEDROOM` – Number of bedrooms  
- `N_BATHROOM` – Number of bathrooms  
- `N_ROOM` – Total rooms  
- `PARK_FACIL` – Park facility availability (Yes/No)  
- `BUILDTYPE` – Type of building (Commercial/House/Other)  
- `UTILITY_AVAIL` – Utility availability  
- `STREET` – Street type  
- `MZZONE` – Market zone  
- `AGE` – Age of building  
- `SALES_PRICE` – Target variable

---

## 📊 Exploratory Data Analysis (EDA)

- Analyzed distributions of numeric columns: `INT_SQFT`, `N_BEDROOM`, `N_BATHROOM`, `AGE`  
- Encoded categorical features: `AREA`, `BUILDTYPE`, `STREET`, `MZZONE`  
- Dropped low-correlation columns: `SALE_COND`, `QS_ROOMS`, `QS_BEDROOM`, `QS_BATHROOM`, `QS_OVERALL`, `DATE_BUILD`, `DATE_SALE`
- 

---

## 🛠 Data Preprocessing

- Missing values handled via **median/mode imputation**  
- Spelling mistakes in categorical columns corrected  
- Created feature `AGE` from `DATE_SALE` and `DATE_BUILD`  
- **Label Encoding:** Ordinal features (`AREA`, `PARK_FACIL`, `UTILITY_AVAIL`, `STREET`, `MZZONE`)  
- **One-Hot Encoding:** Nominal features (`BUILDTYPE`)  
- Standard scaling applied before modeling

---

## 🤖 Modeling

**Algorithms & Performance:**

| Model                  | Parameters / Notes             | R² Score |
|------------------------|--------------------------------|----------|
| Linear Regression       | Default                        | 0.92     |
| K-Nearest Neighbors     | k = 3                          | 0.95     |
| Decision Tree Regressor | Max Depth = 4                  | 0.88     |
| Random Forest Regressor | Max Depth = 4, 100 estimators | 0.87     |
| XGBoost Regressor       | Learning Rate = 0.7, 100 estimators | 0.99 |

> Feature importance analyzed to identify key predictors of house prices.

---

## 📈 Key Insights

- `INT_SQFT`, `N_BEDROOM`, `N_BATHROOM`, `AGE`, `AREA`, and `PARK_FACIL` strongly influence prices  
- Older buildings have lower prices  
- Prime areas (e.g., Anna Nagar, T Nagar) have higher prices  
- Park facilities and street type significantly impact property value

---

## 🔧 Tools & Libraries

- **Python Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`  
- **Visualization:** `matplotlib`, `seaborn`  
- **Modeling:** Linear Regression, KNN, Decision Tree, Random Forest, XGBoost  
