## Overview
In this project, we performed exploratory data preprocessing and built several Support Vector Machine (SVM) classifiers using **linear**, **radial basis function (RBF)**, and **polynomial** kernels to predict cancer occurrence (`CANCEREV`) based on a combination of **demographic** and **habit-related** variables from the NHIS 2022 dataset.

---

## Data Preprocessing
- **Selected Variables**:  
  - **Target**: `CANCEREV`  
  - **Demographic Variables**: `AGE`, `SEX`, `BMICALC`, `EDUC`, `HINOTCOVE`  
  - **Habit Variables**: `HRSLEEP`, `FRUTNO`, `VEGENO`, `COFETEAMNO`  

- **Data Cleaning**:  
  - Removed invalid codes such as 999, 998, etc., replaced them with `NaN`.  
  - Dropped rows with any missing values.  
  - After cleaning, dataset was reduced from the original size to a smaller, clean subset without invalid entries.

---

## Modeling and Evaluation Summary

### Linear SVM
- **Best Parameters**: Tuned `C` through GridSearchCV.
- **Performance**:  
  - **Demographic variables** yielded better predictive performance (higher AUC) than habit-related variables.  
  - **AUC for habits** hovered near 0.5, indicating performance equivalent to random guessing.  
  - **Class imbalance** was evident:  
    - High precision for `No Cancer` class.  
    - Low recall for `Cancer` class.  
  - **Decision Boundary (Age vs. BMI)**:  
    - Boundary is relatively clean but not perfect — due to class imbalance and linear separability limitations.

---

### Radial (RBF) SVM
- **Best Parameters**: Tuned `C` and `gamma`.
- **Performance**:  
  - **Demographic variables** again performed better than habit variables.  
  - Slightly more balanced precision and recall compared to linear SVM.  
  - ROC AUC was decent for demographic variables but habit variables remained close to random.  
  - **Decision Boundary**:  
    - Less interpretable due to the non-linear nature of RBF.  
    - Expected, since RBF kernels capture complex boundaries better, though visual clarity reduces.

---

### Polynomial SVM
- **Best Parameters**: Tuned `C`, `gamma`, `coef0`, with a fixed `degree` of 2.
- **Performance**:  
  - **Demographic variables** outperformed habits again.  
  - Class imbalance still a problem — very low precision and recall for cancer cases.  
  - ROC AUC mirrored patterns seen in other kernels.  
  - **Decision Boundary**:  
    - Produced an oval-shaped, smooth boundary.  
    - More flexible than linear but still constrained by degree 2 polynomial structure.

---

## Key Takeaways
- **Demographic variables are consistently more predictive** of cancer occurrence compared to lifestyle habits based on ROC AUC scores.
- **Severe class imbalance**:  
  - Majority of records are `No Cancer`, making minority class harder to predict.  
  - Models generally performed better for predicting the majority class.
- **Habits as standalone predictors performed poorly**, possibly due to weak or indirect relationships with the outcome variable or poor measurement accuracy.
- **Linear SVM is easier to interpret**, while RBF and Polynomial kernels capture more complex patterns but are harder to visualize, especially with higher-dimensional data.
- **ROC curves** clearly reflected kernel differences — linear and polynomial offered marginal improvements, while RBF better handled non-linearity.

---

## Final Thoughts
- **Potential Improvements**:  
  - Address **class imbalance** using techniques like SMOTE (Synthetic Minority Over-sampling Technique) or class weight adjustments.  
  - Experiment with **feature engineering** (e.g., interaction terms, binning continuous variables).  
  - Explore **other classifiers** (Random Forest, XGBoost) and compare against SVM results.  
  - Perform **multivariate feature selection** to identify strongest predictors.
