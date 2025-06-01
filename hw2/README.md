# Homework 2 – Support Vector Machines: Health Habits & Chronic Disease

This project, part of **Statistical Machine Learning II**, explores how health behaviors and lifestyle factors influence the risk of chronic diseases using **Support Vector Machines (SVMs)**.

📓 Project Notebook: `hw2/hw2.ipynb`

---

## 🧠 Objective

Using data from the **National Health Interview Survey (NHIS)** accessed through **IPUMS Health Survey**, the goal of this project is to predict the presence of chronic illnesses (e.g. cancer, heart disease, stroke, diabetes, heart attack) based on respondents' lifestyle habits and demographics. 

The assignment emphasizes both technical modeling and ethical interpretation of how everyday behaviors relate to major health outcomes.

---

## 📊 Modeling Approach

This project applies **SVM classification models** to predict disease occurrence using combinations of the following health indicators:

- Physical activity levels
- Diet and food consumption habits
- Sleep duration
- Work hours
- Basic demographics (e.g., age, sex, marital status)

The analysis implements and compares three SVM kernels:

1. **Linear kernel**  
   - Interpretable baseline model
2. **Radial basis function (RBF) kernel**  
   - Captures non-linear decision boundaries
3. **Polynomial kernel**  
   - Flexible non-linear interactions

Each model includes:
- Careful variable selection and cleaning
- Standardization and appropriate encoding of predictors
- Hyperparameter tuning (C, gamma, degree)
- Performance evaluation using cross-validation

---

## 🔬 Key Insights

- **Top Predictors**: Sleep duration, physical activity, vegetable consumption, and hours worked per week were among the most consistent predictors of disease.
- **Interpretability**: The linear kernel revealed several intuitive associations, while the RBF kernel better captured complex non-linear relationships.
- **Demographic Subgroup Analysis**: Subsetting by sex and age suggested different patterns in disease risk based on behavior, with certain habits being more predictive in specific populations.

---

## 🧭 Visualization & Ethics

- A hand-crafted **SVM decision boundary plot** demonstrates the classification separation between two key features, illustrating how the margin and support vectors work.
- The poster and notebook include a detailed explanation of:
  - SVM equations and conceptual foundations
  - Kernel function roles
  - Model selection rationale
- Special care is given to avoiding misinterpretation of categorical codes and to **ethical communication** of health-related findings.

---

## 🧾 Deliverables

- 📓 Jupyter Notebook: `hw2/hw2.ipynb` – Includes data cleaning, modeling, and evaluation
- 🖼️ Poster Presentation (submitted separately) – Summarizes methodology, plots, and conclusions in a concise visual format

---

## 🏁 Summary

This project demonstrates the application of **support vector machines** in a real-world healthcare setting. It balances technical rigor with clarity, focusing on:

- Thoughtful variable selection
- Creative hypothesis generation
- Strong model tuning and comparison
- Interpretability and responsibility in presenting health data

It reflects not only technical skills but also critical thinking in modeling design, data ethics, and communication.

