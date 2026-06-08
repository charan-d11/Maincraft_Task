# Maincraft_Task


# 🏡 California Housing Price Prediction

A machine learning project that predicts median house values across California districts using the classic **California Housing dataset**. The project progresses from a Linear Regression baseline to a high-performance **Gradient Boosting model**, paired with rich exploratory and diagnostic visualizations.

---

## 📌 Project Overview

| | |
|---|---|
| **Dataset** | California Housing (sklearn built-in, ~20,640 samples) |
| **Target** | `MedianHouseValue` (in $100,000s) |
| **Baseline Model** | Linear Regression — R² ≈ 0.60 |
| **Improved Model** | Gradient Boosting Regressor — R² ≈ 0.85+ |
| **Language** | Python 3 |

---

## 📁 Project Structure

```
California_Housing/
│
├── California_Housing_Enhanced.ipynb   # Main notebook (EDA + models + visualizations)
└── README.md                           # Project documentation
```

---

## 🔧 Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

| Library | Purpose |
|---|---|
| `numpy` | Numerical operations |
| `pandas` | Data manipulation |
| `matplotlib` | Plotting |
| `seaborn` | Statistical visualizations |
| `scikit-learn` | Dataset, models, metrics, preprocessing |

---

## 📊 Dataset Features

| Feature | Description |
|---|---|
| `MedInc` | Median income in block group |
| `HouseAge` | Median house age in block group |
| `AveRooms` | Average number of rooms per household |
| `AveBedrms` | Average number of bedrooms per household |
| `Population` | Block group population |
| `AveOccup` | Average number of household members |
| `Latitude` | Block group latitude |
| `Longitude` | Block group longitude |
| **`MedianHouseValue`** | **Target — median house value (in $100,000s)** |

---

## 🧪 Notebook Walkthrough

### 1. Data Loading & Inspection
- Loads the California Housing dataset via `sklearn.datasets.fetch_california_housing`
- Checks for null values, data types, and basic statistics

### 2. Exploratory Data Analysis (10 Visualizations)
- **Target Distribution** — histogram + boxplot of `MedianHouseValue`
- **Correlation Heatmap** — feature-to-feature and feature-to-target correlations
- **Feature Distributions** — histograms for all 8 input features
- **Top Features vs Target** — scatter plots for the 4 most correlated features
- **Geographic Price Map** — Latitude/Longitude scatter coloured by house value

### 3. Modelling

**Baseline — Linear Regression**
```python
model = LinearRegression()
model.fit(x_train, y_train)
```

**Improved — Gradient Boosting Regressor**
```python
gbr = GradientBoostingRegressor(
    n_estimators=300,
    learning_rate=0.1,
    max_depth=5,
    subsample=0.8,
    random_state=42
)
```

### 4. Model Evaluation & Comparison
- **Model Comparison Bar Charts** — R² and MAE side-by-side
- **Actual vs Predicted Scatter** — for both models
- **Residual Plots** — prediction error diagnostics
- **Feature Importance** — GBR's top contributing features
- **5-Fold Cross-Validation** — fold-wise R² scores with mean

---

## 📈 Results

| Metric | Linear Regression | Gradient Boosting |
|---|---|---|
| **R² Score** | ~0.60 | **~0.85+** |
| **MAE** | ~0.53 | **~0.37** |
| **MSE** | ~0.55 | **~0.23** |

> The Gradient Boosting model delivers a **~40% improvement in R²** over the Linear Regression baseline.

---

## 🚀 How to Run

1. Clone or download this repository
2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```
3. Open the notebook:
   ```bash
   jupyter notebook California_Housing_Enhanced.ipynb
   ```
4. Run all cells — the dataset downloads automatically via sklearn

---

## 💡 Key Insights

- **`MedInc` (Median Income)** is the strongest single predictor of house value
- **Geography matters** — coastal and Bay Area districts command significantly higher prices
- Gradient Boosting captures non-linear feature interactions that Linear Regression misses
- Cross-validation confirms the GBR generalizes well across folds (low variance)

---

## 🔭 Possible Next Steps

- Hyperparameter tuning with `GridSearchCV` or `Optuna`
- Try `XGBoost` or `LightGBM` for further performance gains
- Add polynomial features or interaction terms for Linear Regression
- Deploy the model as a simple web app using `Streamlit` or `Flask`