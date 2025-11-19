

---

# **Task 1 – Data Cleaning (Titanic Dataset)**

This project focuses on cleaning and preprocessing the Titanic dataset as part of an internship task.
The goal is to convert the raw dataset into a clean, structured, and machine-learning-ready format.

---

## **Objectives**

* Handle missing values
* Encode categorical data
* Detect and remove outliers
* Standardize numerical columns
* Save a fully cleaned dataset

---

## **Data Cleaning Steps**

### 1. Data Loading and Initial Exploration

* Loaded the dataset using pandas
* Checked shape, datatypes, missing values, and descriptive statistics

### 2. Handling Missing Values

| Column   | Method Used                                      |
| -------- | ------------------------------------------------ |
| Age      | Filled with median                               |
| Embarked | Filled with mode                                 |
| Cabin    | Filled with "Unknown" due to many missing values |

---

### 3. Encoding Categorical Variables

| Column   | Encoding Method                         |
| -------- | --------------------------------------- |
| Sex      | Label Encoding (male = 0, female = 1)   |
| Embarked | One-Hot Encoding                        |
| Title    | Extracted from Name and one-hot encoded |

---

### 4. Outlier Detection and Removal

Outliers were identified using the Interquartile Range (IQR) method.
The formula used:

```
Outlier if:
x < Q1 - 1.5 * IQR
or
x > Q3 + 1.5 * IQR
```

This was applied mainly to the Fare column.

---

### 5. Feature Scaling

StandardScaler was used to scale:

* Age
* Fare

This ensures numerical values are normalized for modeling.

---

### 6. Saving the Cleaned Dataset

The final dataset was exported as:

```
cleaned_titanic.csv
```

The file contains:

* No missing values
* Encoded categorical columns
* Standardized numerical columns
* All numeric and clean features

---

## **Final Results**

| Step                    | Status    |
| ----------------------- | --------- |
| Missing values handled  | Completed |
| Categorical encoding    | Completed |
| Outlier removal         | Completed |
| Feature scaling         | Completed |
| Cleaned dataset created | Completed |

---

| File Name             | Description                                                                                                                                    |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `tapo.ipynb`          | Jupyter Notebook containing the full data-cleaning workflow for the Titanic dataset.                                                           |
| `cleaned_titanic.csv` | Final cleaned dataset produced after handling missing values, encoding categorical features, removing outliers, and scaling numerical columns. |
| `README.md`           | Documentation describing the objectives, steps, and results of Task 1.                                                                         |
