# Machine Learning Zoomcamp — Homework 4: Evaluation Metrics for Classification

Lead scoring: predict whether a lead will convert into a customer, and evaluate the model with ROC AUC, precision, recall, F1 and cross-validation.

## Files

| File | Description |
|---|---|
| `homework.ipynb` | Notebook with the code and outputs for all questions |
| `course_lead_scoring_2026.csv` | Dataset (not included here, download it from the course page) |

## Dataset

Target: `converted` (1 = the lead converted, 0 = did not convert).

| Type | Columns |
|---|---|
| Categorical | `lead_source`, `industry`, `employment_status`, `location` |
| Numerical | `annual_income`, `number_of_courses_viewed`, `interaction_count`, `lead_score` |

## Data preparation

- Missing values: categorical columns filled with `'NA'`, numerical columns filled with `0.0`.
- Split with `train_test_split` and `random_state=1`: 60% train / 20% validation / 20% test (3000 / 1000 / 1000 rows).
- The target `converted` is separated from the features (`y_train`, `y_val`, `y_test`) and removed from the dataframes.


## Tools

Python, pandas, NumPy, scikit-learn (`LogisticRegression`, `DictVectorizer`, `KFold`, `roc_auc_score`), matplotlib.
