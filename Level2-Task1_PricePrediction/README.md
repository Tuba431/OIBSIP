# Task 1: House Price Prediction Model

## 📋 Task Information

| Field | Details |
|-------|---------|
| **Level Number** | Level 2 |
| **Task Number** | Task 1 |
| **Submitted By** | Tuba |
| **File Name** | Tuba_Task4.ipynb |
| **Submission Date** | July 2026 |
| **Repository** | [OIBSIP](https://github.com/your-username/OIBSIP) |

---

## 🎯 Objective

Build a machine learning model to predict house prices based on various features such as area, number of rooms, parking, warehouse, elevator, and location.

---

## ✅ Feature Checklist

| Feature | Status | Details |
|---------|--------|---------|
| [x] Load dataset and EDA | ✅ Done | Data inspection, statistics, visualization |
| [x] Handle missing values | ✅ Done | Median imputation for numeric columns |
| [x] Encode categorical variables | ✅ Done | One-Hot Encoding for Location_Type |
| [x] Feature selection & correlation | ✅ Done | Correlation heatmap |
| [x] Train/Test split | ✅ Done | 80% train, 20% test |
| [x] Build preprocessing pipeline | ✅ Done | StandardScaler for numeric features |
| [x] Train Linear Regression | ✅ Done | Base model |
| [x] Evaluate Linear Regression | ✅ Done | MSE, RMSE, R² Score |
| [x] Residual analysis | ✅ Done | Residual plot |
| [x] Train Ridge Regression | ✅ Done | Regularization model |
| [x] Train Lasso Regression | ✅ Done | Feature selection model |
| [x] Model comparison | ✅ Done | Summary table |
| [x] Visualizations | ✅ Done | Scatter plot, residual plot, correlation heatmap |

---

## 📊 Dataset Information

| Attribute | Details |
|-----------|---------|
| **Source** | House Price Dataset |
| **Rows** | 1,000 (synthetic data) |
| **Features** | Area, Bedrooms, Bathrooms, Floors, Age, Location_Score, Garage, Renovated, Location_Type |
| **Target** | Price |

---

## 🔍 Model Performance Comparison

| Model | MSE | RMSE | R² Score |
|-------|-----|------|----------|
| **Linear Regression** | [value] | [value] | [value] |
| **Ridge Regression** | [value] | [value] | [value] |
| **Lasso Regression** | [value] | [value] | [value] |

### Key Observations
- Ridge and Lasso regressions help reduce overfitting compared to Linear Regression
- Lasso regression performs feature selection by shrinking coefficients to zero

---

## 📈 Visualizations

### 1. Actual vs Predicted Prices
![Actual vs Predicted](images/Actual_vs_Predicted.png)
*Scatter plot showing model performance*

### 2. Residual Plot
![Residuals](images/Residual_Plot.png)
*Residual analysis for model validation*

### 3. Correlation Heatmap
![Correlation](images/Correlation_Heatmap.png)
*Feature correlation with target variable*

### 4. Feature Importance
![Feature Importance](images/Feature_Importance.png)
*Top features influencing house prices*

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.8+** | Programming language |
| **Pandas** | Data manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical visualization |
| **Scikit-learn** | Machine learning models |

---

