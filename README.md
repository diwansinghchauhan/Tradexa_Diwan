# Summary of Approach

## 1. Modeling and Allocation
- **Data Cleaning:** Removed outliers in `3YrReturn%` using IQR filtering.
- **Feature Engineering:** Created `Assets × Sharpe Ratio`, encoded star ratings (1–5), and included 1-year returns.
- **Model Training:** Tuned a Random Forest with 5-fold RandomizedSearchCV.
  - Best CV R²: 0.750  
  - Test RMSE: 1.357  
  - Test R²: 0.728

**Optimal Allocation:**  
Allocate **100%** to **Mid-Cap / Value / High**  
Predicted **3YrReturn%:** 19.29%

## 2. Validation of Efficiency
- **Cross-Validation:** 5-fold CV yielded R² ≈ 0.750.
- **Hold-out Test:** Achieved R² ≈ 0.728 and RMSE ≈ 1.357 on unseen data.

## 3. Visualizations

### Distribution of 3-Year Returns
<img width="1580" height="1014" alt="Image" src="https://github.com/user-attachments/assets/78a5852e-d3dd-406e-8007-511c90f3776e" />

### 3-Year Returns by Risk Category
![3YrReturn% by Risk](boxplot_risk_3yrreturn.png)
