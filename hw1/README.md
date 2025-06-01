# Homework 1 – Tree-Based Models: Predicting Youth Drug Use

This project was completed for **Statistical Machine Learning II** and focuses on applying decision tree-based models to analyze youth drug use patterns using data from the **National Survey on Drug Use and Health (NSDUH)**.

📓 Project Notebook: `hw1/hw1.ipynb`

---

## 🧠 Objective

The primary goal of this assignment was to investigate **factors associated with youth drug use** using interpretable, tree-based machine learning models. Working with real-world national survey data, the project explores multiple supervised learning frameworks and addresses the complexities of high-dimensional behavioral data.

---

## 🔍 Project Focus

- **Data**: A cleaned and pre-processed subset of the NSDUH 2023 dataset focusing on youth under 18, including:
  - Demographics (e.g., age, gender, income)
  - Substance use patterns (e.g., usage frequency, age of first use)
  - Social and environmental context (e.g., peer influence, parental monitoring, school engagement)
- **Research Question**: What factors best predict youth substance use behavior, and how can tree-based models help interpret those relationships?

---

## 🛠️ Modeling Techniques

The project covers three types of supervised learning tasks:

1. **Binary Classification**  
   - Predicting whether a youth has ever smoked cigarettes  
   - Models: Decision Tree, Random Forest

2. **Multi-Class Classification**  
   - Categorizing marijuana usage frequency  
   - Models: XGBoost, Gradient Boosting Classifier

3. **Regression**  
   - Estimating number of days alcohol was consumed in the past year  
   - Models: Decision Tree Regressor

All models include:
- Hyperparameter tuning
- Evaluation metrics (accuracy, F1 score, RMSE)
- Comparisons between ensemble and baseline methods

---

## 🌳 Interpretability & Results

- Visualizations of decision trees with human-readable labels
- Detailed analysis of selected paths and end nodes within trees
- Comparison of feature encodings (binary vs ordinal vs continuous) and their impact on model predictions
- Feature importance analysis revealing key predictors such as:
  - Peer and parental influence
  - School attendance and performance
  - Socioeconomic status

---

## 🧭 Ethical Reflections

The project includes a section on **ethical interpretation and communication**:
- The risks of overfitting behavioral patterns to sensitive traits
- Importance of context when modeling real-world social data
- Recommendations for responsible data storytelling when working with youth-related health data

---

## 🎥 Presentation

A recorded video presentation (7–10 minutes) complements the code and provides:
- A walkthrough of the modeling approach
- Discussion of key findings and visualizations
- Ethical considerations in communicating sensitive results

---

## 📂 Key Files

- `hw1/hw1.ipynb`: Main analysis and modeling notebook
- `youth_data.csv`: Pre-processed survey data (optional if you prefer using the `.Rdata` version)
- Codebook (linked externally in the notebook) for understanding survey variables

---

## 🏁 Summary

This assignment demonstrates the practical application of decision trees and ensemble models in a high-dimensional, real-world setting. Key strengths of the project include:
- Strong interpretability through tree-based modeling
- Careful treatment of variable types and encoding
- Thoughtful reflection on ethical data science practices

