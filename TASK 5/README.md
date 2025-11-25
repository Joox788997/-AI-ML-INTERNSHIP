# Task 5 — Decision Trees & Random Forests

## Project Summary
Build and evaluate tree-based models (Decision Tree and Random Forest) for a binary classification problem using the StudentsPerformance dataset.

---

## Dataset
| Attribute | Value |
|-----------|-------|
| File | StudentsPerformance.csv |
| Samples | (see notebook) |
| Features | gender, race/ethnicity, parental level of education, lunch, test preparation course, math, reading, writing |
| Target (engineered) | pass_math: 1 if math score >= 60 else 0 (binary classification) |

---

## Repository Structure
| File | Description |
|------|-------------|
| `task5.ipynb` | Notebook with full pipeline (preprocessing, modeling, evaluation) |
| `task5_random_forest.pkl` | Trained Random Forest model (serialized) |
| `task5_decision_tree_best.pkl` | Trained Decision Tree (best depth) |
| `task5_predictions.csv` | Predictions and ground truth |
| `README.md` | This documentation |

---

## Pipeline Steps (high-level)
| Step | Action |
|------|--------|
| 1 | Load dataset and inspect |
| 2 | Create binary target `pass_math` |
| 3 | One-hot encode categorical features |
| 4 | Split data (80/20) with stratification |
| 5 | Train Decision Tree (baseline) |
| 6 | Visualize and constrain tree depth to prevent overfitting |
| 7 | Train Random Forest and evaluate |
| 8 | Plot feature importances |
| 9 | Cross-validation for robust accuracy estimate |
| 10 | Save models & predictions |

---

## Evaluation Summary
| Model | Test Accuracy | CV Mean (5-fold) |
|-------|---------------|------------------|
| Decision Tree (best depth) | see notebook | see notebook |
| Random Forest | see notebook | see notebook |

> Detailed classification reports and confusion matrices are provided inside the notebook.

---



