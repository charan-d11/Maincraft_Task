# 🏠 AI/ML Task 2: Model Comparison for House Price Prediction

## 📌 Overview

This project focuses on building and comparing multiple machine learning models to predict house prices using the **California Housing Dataset**. The goal is to evaluate different regression algorithms and identify the best-performing model based on key metrics.

---

## 📂 Dataset

* **Source**: `sklearn.datasets.fetch_california_housing`
* Contains features like:

  * Median Income
  * House Age
  * Average Rooms
  * Population
  * Latitude & Longitude
* **Target Variable**: House Price

---

## ⚙️ Technologies Used

* Python 🐍
* Pandas & NumPy
* Scikit-learn
* Matplotlib

---

## 🔄 Workflow

1. **Data Loading**

   * Imported dataset using sklearn
   * Converted into a DataFrame

2. **Data Preprocessing**

   * Feature-target split
   * Standardization using `StandardScaler`

3. **Train-Test Split**

   * 80% training and 20% testing data

4. **Model Training**
   The following models were implemented:

   * Linear Regression
   * Decision Tree Regressor (max_depth=5)
   * Ridge Regression

5. **Model Evaluation**
   Models were evaluated using:

   * RMSE (Root Mean Squared Error)
   * R² Score

6. **Final Model**

   * Linear Regression selected as final model
   * Predictions visualized using scatter plot

---

## 📊 Results

| Model             | RMSE | R² Score |
| ----------------- | ---- | -------- |
| Linear Regression | ✔️   | ✔️       |
| Decision Tree     | ✔️   | ✔️       |
| Ridge Regression  | ✔️   | ✔️       |

(*Exact values can be seen in the notebook*)

---

## 📈 Visualization

* Scatter plot of **Actual vs Predicted House Prices**
* Helps in understanding model accuracy visually

---



## 📌 Key Learnings

* Importance of feature scaling
* Comparison of regression models
* Evaluating models using RMSE and R²
* Visual interpretation of predictions

---

## 🔮 Future Improvements

* Hyperparameter tuning
* Add more models (Random Forest, XGBoost)
* Cross-validation
* Feature engineering

---

## 👨‍💻 Author

**Durgacharan Mallick**

---

