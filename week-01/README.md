# Week 01 — Foundations, Data Cleaning, EDA & Machine Learning Foundations

> **Engineering journal:** inspect, transform, prepare, and evaluate data through a reproducible workflow.

This folder contains the practical work from the first week of my Data Science & Data Engineering Bootcamp. The Titanic dataset is used to practice data quality, exploratory analysis, feature engineering, preprocessing, and introductory classification.

---

## Day 03 — Titanic Data Cleaning

**Notebook:** [day3_titanic_cleaning.ipynb](day3_titanic_cleaning.ipynb)

- Inspected dataset dimensions and missing-value patterns.
- Removed `deck` because of its high proportion of missing values.
- Filled missing `age` values with the median.
- Removed records missing `embarked` and removed exact duplicate rows.
- Compared missing values before and after cleaning.

**Engineering takeaway:** cleaning is a sequence of explainable decisions, not a mechanical checklist.

---

## Day 04 — Exploratory Data Analysis & Data Visualization

**Notebook:** [day4_titanic_visualization.ipynb](day4_titanic_visualization.ipynb)

- Created an age histogram with KDE.
- Compared ticket fares across passenger classes with a boxplot.
- Built a numerical correlation heatmap.
- Interpreted distributions, outliers, and associations without treating correlation as causation.

**Engineering takeaway:** visual exploration helps reveal data patterns and questions before modeling.

---

## Day 05 — Feature Engineering & Data Encoding

**Notebook:** [day5_feature_engineering.ipynb](day5_feature_engineering.ipynb)

- Applied binary mapping to the `sex` feature.
- Applied one-hot encoding to the nominal `embarked` feature.
- Used `drop_first=True` to select a reference category.
- Concatenated encoded columns and validated the resulting schema.

**Engineering takeaway:** feature representations should preserve meaning rather than inventing an artificial order between categories.

---

## Day 06 — Data Preprocessing & Machine Learning Pipeline

**Notebook:** [day6_data_preprocessing_pipeline.ipynb](day6_data_preprocessing_pipeline.ipynb)

- Prepared the numerical feature matrix and binary survival target.
- Split the data into 80% training and 20% testing subsets with stratification.
- Built a Scikit-learn pipeline using median imputation and standard scaling.
- Fitted preprocessing only on training data and transformed the test set with the learned parameters.

**Engineering takeaway:** fitting preprocessing on the full dataset causes data leakage. Split first, fit on training data, and only transform held-out data.

---

## Day 07 — Model Training & Evaluation

**Notebook:** [day7_model_training_evaluation.ipynb](day7_model_training_evaluation.ipynb)

- Trained Logistic Regression as a baseline classifier.
- Trained a Random Forest classifier with 100 trees and a maximum depth of 5.
- Evaluated both models using accuracy, confusion matrices, and classification reports.
- Compared precision, recall, F1-score, and support rather than relying on accuracy alone.

**Engineering takeaway:** a model should be evaluated on unseen data, and model quality must be judged using metrics that reflect the problem.

---

## Week 01 Structure

```text
week-01/
├── images/
│   ├── age_distribution.svg
│   ├── fare_by_class_boxplot.svg
│   └── correlation_heatmap.svg
├── day3_titanic_cleaning.ipynb
├── day4_titanic_visualization.ipynb
├── day5_feature_engineering.ipynb
├── day6_data_preprocessing_pipeline.ipynb
├── day7_model_training_evaluation.ipynb
└── README.md
```

## Tools Used

- **Python** — analysis and scripting
- **Pandas** — data inspection and transformation
- **Seaborn** — sample dataset and statistical visualization
- **Matplotlib** — visualization
- **Scikit-learn** — preprocessing, pipelines, classification, and evaluation
- **Jupyter Notebook / Google Colab** — interactive experiments
- **Git & GitHub** — version control and documentation

---

*Week 01 is a foundation: understand the data, preserve its integrity, and make every analytical decision explainable.*
