# Week 01 — Data Science Foundations to Machine Learning

> **From understanding data to preparing it, exploring it, and training baseline models.**

This week is structured as a progressive learning path. The first two days establish the Python data-analysis environment and core libraries. Days 03–07 apply those foundations to the Titanic dataset and introduce the first machine-learning workflow.

---

## Learning Path — Day 01 to Day 07

### Day 01 — Data Science Foundations, Work Environment & NumPy

**Notebook:** [day1_data_science_numpy.ipynb](day1_data_science_numpy.ipynb)

- Understand the stages of a data science project.
- Set up Google Colab or Jupyter Notebook.
- Create NumPy arrays and perform vectorized operations.
- Explore `shape`, `dtype`, and `ndim`.
- Create arrays, use indexing and slicing, and filter with Boolean masks.
- Understand `axis=0`, `axis=1`, and independent copies.

**Engineering takeaway:** NumPy provides efficient array operations and the numerical foundation used by many data-science libraries.

### Day 02 — Data Analysis with Pandas

**Notebook:** [day2_pandas_fundamentals.ipynb](day2_pandas_fundamentals.ipynb)

- Understand Series and DataFrame.
- Read tabular data and inspect its shape, columns, data types, and summary statistics.
- Select rows and columns with brackets, `loc`, and `iloc`.
- Filter, create columns, sort, and count values.
- Aggregate data with `groupby`.
- Join tables with `merge` and summarize with `pivot_table`.
- Recognize common copy and assignment warnings.

**Engineering takeaway:** Pandas turns raw tabular data into something that can be inspected, filtered, transformed, and summarized systematically.

### Day 03 — Titanic Data Cleaning

**Notebook:** [day3_titanic_cleaning.ipynb](day3_titanic_cleaning.ipynb)

- Inspect dataset dimensions and missing-value patterns.
- Remove `deck` because of its high proportion of missing values.
- Fill missing `age` values with the median.
- Remove records missing `embarked` and remove exact duplicate rows.
- Compare missing values before and after cleaning.

**Engineering takeaway:** cleaning is a sequence of explainable decisions, not a mechanical checklist.

### Day 04 — Exploratory Data Analysis & Data Visualization

**Notebook:** [day4_titanic_visualization.ipynb](day4_titanic_visualization.ipynb)

- Create an age histogram with KDE.
- Compare fares across passenger classes with a boxplot.
- Build a numerical correlation heatmap.
- Interpret distributions, outliers, and associations without treating correlation as causation.

**Engineering takeaway:** visual exploration helps reveal data patterns and questions before modeling.

### Day 05 — Feature Engineering & Data Encoding

**Notebook:** [day5_feature_engineering.ipynb](day5_feature_engineering.ipynb)

- Apply binary mapping to the `sex` feature.
- Apply one-hot encoding to the nominal `embarked` feature.
- Use `drop_first=True` to select a reference category.
- Concatenate encoded columns and validate the resulting schema.

**Engineering takeaway:** feature representations should preserve meaning rather than inventing an artificial order between categories.

### Day 06 — Data Preprocessing & Machine Learning Pipeline

**Notebook:** [day6_data_preprocessing_pipeline.ipynb](day6_data_preprocessing_pipeline.ipynb)

- Prepare the numerical feature matrix and binary survival target.
- Split the data into 80% training and 20% testing subsets with stratification.
- Build a Scikit-learn pipeline using median imputation and standard scaling.
- Fit preprocessing only on training data and transform the test set with learned parameters.

**Engineering takeaway:** split first, fit preprocessing on training data, and transform held-out data to prevent data leakage.

### Day 07 — Model Training & Evaluation

**Notebook:** [day7_model_training_evaluation.ipynb](day7_model_training_evaluation.ipynb)

- Train Logistic Regression as a baseline classifier.
- Train a Random Forest classifier with 100 trees and a maximum depth of 5.
- Evaluate both models using accuracy, confusion matrices, and classification reports.
- Compare precision, recall, F1-score, and support rather than relying on accuracy alone.

**Engineering takeaway:** evaluate models on unseen data and choose metrics that reflect the problem, not just a single score.

---

## Week 01 Structure

```text
week-01/
├── images/
│   ├── age_distribution.png
│   ├── fare_by_class_boxplot.png
│   └── correlation_heatmap.png
├── day1_data_science_numpy.ipynb
├── day2_pandas_fundamentals.ipynb
├── day3_titanic_cleaning.ipynb
├── day4_titanic_visualization.ipynb
├── day5_feature_engineering.ipynb
├── day6_data_preprocessing_pipeline.ipynb
├── day7_model_training_evaluation.ipynb
└── README.md
```

## Tools Used

- **Python** — analysis and scripting
- **NumPy** — numerical arrays and vectorized operations
- **Pandas** — data inspection and transformation
- **Seaborn & Matplotlib** — sample data and visualization
- **Scikit-learn** — preprocessing, pipelines, classification, and evaluation
- **Jupyter Notebook / Google Colab** — interactive experiments
- **Git & GitHub** — version control and documentation

---

## End-of-Week Outcome

By the end of this week, the learning path moves from core data tools to an initial classification workflow: inspect and clean a dataset, explore it visually, encode selected features, prepare train/test data without leakage, and compare baseline models.

*Week 01 is a foundation: understand the data, preserve its integrity, and make every analytical decision explainable.*
