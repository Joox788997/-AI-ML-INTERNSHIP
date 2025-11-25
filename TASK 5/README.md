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


| File name                      | Purpose / Description                                                                                                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `task5.ipynb`                  | Jupyter Notebook with the full pipeline: loading data, preprocessing, Decision Tree and Random Forest training, visualization, cross-validation, evaluation, and saving outputs.       |
| `StudentsPerformance.csv`      | Dataset used for the task. Local path: `/mnt/data/StudentsPerformance.csv`. (Use this file as the dataset source when running the notebook.)                                           |
| `task5_random_forest.pkl`      | Serialized Random Forest model (saved with `joblib.dump`). Optional but recommended to include for reproducibility.                                                                    |
| `task5_decision_tree_best.pkl` | Serialized Decision Tree model with the selected `max_depth`.                                                                                                                          |
| `task5_predictions.csv`        | CSV with test set ground truth and predictions (columns: `y_true`, `pred_rf`, `pred_tree`).                                                                                            |
| `README.md`                    | Project documentation: objectives, steps, results, how to run, and brief answers to interview questions.                                                                               |
| `plots/` (folder)              | Optional folder containing exported plot images: `confusion_matrix.png`, `roc_curve.png`, `feature_importance.png`, `tree_plot.png`. (Include if you export images from the notebook.) |
| `requirements.txt`             | (optional) Exact Python packages and versions used, e.g.: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `joblib`.                                                        |

