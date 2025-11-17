.

---


# **Task 2 – Exploratory Data Analysis (Titanic Dataset)**

This project performs Exploratory Data Analysis (EDA) on the Titanic dataset as part of an internship assignment.
The objective is to understand the structure, distribution, relationships, and patterns within the data before applying machine learning.

---

## **Objectives**

* Load and inspect the dataset
* Generate summary statistics
* Analyze distributions of numerical features
* Detect and visualize outliers
* Explore relationships between features
* Visualize correlations
* Extract insights and patterns from the data

---

## **Files Included**

| File Name                             | Description                                       |
| ------------------------------------- | ------------------------------------------------- |
| `task2_eda.ipynb`                     | Jupyter Notebook containing the full EDA workflow |
| `titanic.csv` / `cleaned_titanic.csv` | Dataset used for analysis                         |
| `README.md`                           | Documentation for Task 2                          |

---

## **Steps Performed**

### **1. Data Loading and Basic Information**

* Inspected shape, datatypes, and missing values
* Displayed summary statistics
* Checked for duplicates and overall structure

---

### **2. Distribution Analysis**

Histograms and KDE plots were generated for major numerical features, including:

* Age
* Fare
* SibSp
* Parch

These visualizations helped understand spread, skewness, and overall behavior of variables.

---

### **3. Outlier Detection**

Boxplots were used to identify outliers in:

* Age
* Fare

Outliers were visually inspected to understand their impact.

---

### **4. Correlation Analysis**

A numeric-only correlation matrix was generated and visualized using a heatmap to identify relationships between features such as:

* Survived
* Pclass
* Sex
* Fare
* Age

A pairplot was also used to observe multi-feature relationships.

---

### **5. Categorical Analysis**

Countplots were used to explore survival patterns based on:

* Sex
* Passenger class (Pclass)
* Embarkation point

---

### **6. Key Insights**

* Females had a significantly higher survival rate than males.
* Passengers in 1st class survived more than those in 2nd and 3rd.
* Higher fare values were associated with a higher chance of survival.
* Younger passengers showed slightly better survival patterns.
* Sex, Pclass, and Fare were among the strongest predictors based on correlation.

---

## **Conclusion**

This EDA provides a detailed understanding of the Titanic dataset by exploring distributions, patterns, correlations, and outliers.
The insights gained from this analysis help prepare the dataset for machine learning models in future task
