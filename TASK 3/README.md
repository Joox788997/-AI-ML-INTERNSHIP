

# **Task 3 – Linear Regression (AI & ML Internship)**

### **A complete implementation and analysis of simple and multiple linear regression using Scikit-learn**

---

## **1. Project Overview**

This project applies both **Simple Linear Regression** and **Multiple Linear Regression** on the **House Price Prediction Dataset**.
The goal is to understand:

* Data preprocessing
* Model training
* Feature selection
* Evaluation metrics (MAE, MSE, R²)
* Coefficient interpretation
* Visualization of predictions and residuals

This task demonstrates core supervised learning foundations required in machine learning pipelines.

---

## **2. Dataset Description**

Dataset used: **housing.csv**

| Feature                  | Description                |
| ------------------------ | -------------------------- |
| longitude                | Geographic coordinate      |
| latitude                 | Geographic coordinate      |
| housing_median_age       | Median age of houses       |
| total_rooms              | Total number of rooms      |
| total_bedrooms           | Total number of bedrooms   |
| population               | Population in the district |
| households               | Number of households       |
| median_income            | Median income              |
| median_house_value       | Target variable (price)    |
| ocean_proximity          | Categorical location label |
| rooms_per_household      | Engineered feature         |
| bedrooms_per_room        | Engineered feature         |
| population_per_household | Engineered feature         |

---

## **3. Files in Repository**

| File Name                | Description                                                                                    |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| `task3.ipynb`            | Full Jupyter Notebook containing preprocessing, model training, evaluation, and visualizations |
| `housing.csv`            | Dataset used in the project                                                                    |
| `task3_predictions.csv`  | Saved results containing actual vs predicted values                                            |
| `task3_linear_model.pkl` | Trained regression model (optional export)                                                     |
| `README.md`              | Documentation for Task 3                                                                       |

---

## **4. Methodology**

The project follows a standard end-to-end machine learning workflow.

---

### **4.1 Data Preprocessing**

Steps include:

* Handling missing values (`total_bedrooms → median`)
* One-hot encoding of `ocean_proximity`
* Feature engineering to improve model learning:

  * `rooms_per_household`
  * `bedrooms_per_room`
  * `population_per_household`
* Basic statistical summary and dataset inspection

---

### **4.2 Feature Selection**

Two designs were evaluated:

**Simple Regression (1 feature):**
`median_income → median_house_value`

**Multiple Regression (5+ features):**

* `median_income`
* `housing_median_age`
* `total_rooms`
* `rooms_per_household`
* `bedrooms_per_room`
* One-hot encoded location features (if present)

This allows comparison between simple vs multivariate modeling.

---

### **4.3 Train–Test Split**

* 80% Training
* 20% Testing
* `random_state = 42` to ensure reproducibility

---

### **4.4 Feature Scaling**

Used **StandardScaler** to normalize numerical values.
Scaling ensures the model treats all features equally, especially when magnitudes differ.

---

### **4.5 Model Training**

Model used:

```
LinearRegression()
```

Fitted using:

```
model.fit(X_train_scaled, y_train)
```

---

### **4.6 Model Evaluation**

Metrics computed:

| Metric | Meaning                                |
| ------ | -------------------------------------- |
| MAE    | Average absolute prediction error      |
| MSE    | Squared error (penalizes large errors) |
| R²     | How much variance the model explains   |

These metrics help evaluate prediction accuracy and model fitness.

---

### **4.7 Visualizations**

The notebook includes:

* **Actual vs Predicted Scatter Plot**
* **Regression Line** (Simple Regression only)
* **Residual Distribution Plot**
* **Residuals vs Predicted Plot**

These visual tools help diagnose model quality.

---

### **4.8 Coefficient Interpretation**

Extracted:

* Intercept
* Coefficients for each feature

Interpretation example:
A positive coefficient indicates the target value increases as the feature increases (holding other features constant).

---

## **5. Results Summary**

Key observations:

* The model captures broad patterns in house prices.
* **Median Income** showed the strongest positive correlation with house prices.
* Additional engineered features improved performance compared to single-feature regression.
* Residual analysis showed clear non-linear patterns, suggesting housing prices have factors beyond linear relationships.

---

## **6. How to Run Locally**

1. Upload `housing.csv` to your Jupyter directory.
2. Open `task3.ipynb` in Jupyter Lab/Notebook.
3. Run all cells from start to finish.
4. Outputs will be generated:

   * Evaluation metrics
   * Plots
   * `task3_predictions.csv`
   * `task3_linear_model.pkl`

---

## **7. Conclusion**

This task provides hands-on understanding of:

* Linear regression fundamentals
* Data preprocessing & feature engineering
* Model evaluation using standard metrics
* Visual analysis and coefficient interpretation

The project establishes the foundation for more advanced machine learning workflows such as regularization, decision trees, or neural networks.

---


