# Data Science & Data Engineering Bootcamp
### An Engineering Journal — From Full-Stack Systems to Data-Driven Thinking

> **Build with purpose. Automate with intention. Treat data as a first-class engineering asset.**

Welcome to my **Data Science & Data Engineering Bootcamp** repository — a living record of my transition from building full-stack applications and intelligent automation systems to developing a deeper, more rigorous understanding of data.

My background is rooted in software engineering: designing application workflows, integrating APIs, building automation pipelines, and turning ideas into working products. That experience shaped the way I approach this new chapter. I don't see data science as a collection of notebooks or isolated algorithms; I see it as an engineering discipline that starts with trustworthy data, clear assumptions, reproducible workflows, and systems that solve real problems.

My philosophy is **automation-first, clean architecture, and data integrity**. I want every experiment to be understandable, every transformation to have a reason, and every result to be reproducible. This repository is where I document not only what I learn, but also the decisions, trade-offs, mistakes, and engineering lessons behind the work.

The goal is to build a practical portfolio that demonstrates steady progress — from data foundations and exploratory analysis toward reliable data workflows, machine learning, and data engineering practices.

---

## Repository Structure

```text
data-science-bootcamp/
├── week-01/
│   ├── images/
│   ├── day3_titanic_cleaning.ipynb
│   ├── day4_titanic_visualization.ipynb
│   ├── day5_feature_engineering.ipynb
│   ├── day6_data_preprocessing_pipeline.ipynb
│   ├── day7_model_training_evaluation.ipynb
│   └── README.md
├── week-02/
│   └── ...
├── week-03/
│   └── ...
└── README.md
```

> The structure evolves as the bootcamp progresses. New deliverables are added when their work is ready, rather than filled with empty placeholders.

---

## Weekly Progress & Engineering Journey

### Week 01 — Foundations, Data Cleaning, EDA & Machine Learning

**Theme: Before asking data for answers, make sure it deserves your trust.**

The first stage uses the classic **Titanic dataset** to build a disciplined workflow: inspect data quality, explore distributions, engineer model-ready features, prepare data without leakage, and evaluate baseline classifiers.

#### Day 03 — Titanic Data Cleaning

**Notebook:** [day3_titanic_cleaning.ipynb](week-01/day3_titanic_cleaning.ipynb)

Loaded the Titanic dataset with Seaborn, inspected dimensions and missing values, removed the high-missingness `deck` column, imputed missing ages with the median, handled missing embarkation records, and removed exact duplicates.

#### Day 04 — Exploratory Data Analysis & Visualization

**Notebook:** [day4_titanic_visualization.ipynb](week-01/day4_titanic_visualization.ipynb)

Created an age histogram with KDE, a fare-by-class boxplot, and a numerical correlation heatmap. The visual analysis highlights distribution shape, fare differences between passenger classes, and associations between selected numerical features.

#### Day 05 — Feature Engineering & Data Encoding

**Notebook:** [day5_feature_engineering.ipynb](week-01/day5_feature_engineering.ipynb)

Converted `sex` into a binary numerical feature and applied one-hot encoding to `embarked`. The notebook explains the reference category and why nominal categories should not be assigned arbitrary ordinal values.

#### Day 06 — Data Preprocessing & Pipeline

**Notebook:** [day6_data_preprocessing_pipeline.ipynb](week-01/day6_data_preprocessing_pipeline.ipynb)

Prepared the feature matrix and survival target, created a stratified 80/20 train/test split, and built a Scikit-learn pipeline with median imputation and standard scaling. The preprocessing steps are fitted on training data only to prevent data leakage.

#### Day 07 — Model Training & Evaluation

**Notebook:** [day7_model_training_evaluation.ipynb](week-01/day7_model_training_evaluation.ipynb)

Trained Logistic Regression and Random Forest classifiers. Evaluated predictions using accuracy, confusion matrices, and classification reports, then compared the models while considering precision, recall, and F1-score.

#### What this week is teaching me

- Inspect first; transform second.
- Make feature engineering explicit and preserve category meaning.
- Split before fitting preprocessing steps to avoid data leakage.
- Establish baseline models before increasing complexity.
- Evaluate models with more than one metric and keep the test set unseen.

---

## Tech Stack & Tools

| Tool | Role in this repository |
|---|---|
| **Python** | Primary language for data analysis and engineering workflows |
| **Pandas** | Data loading, inspection, transformation, and cleaning |
| **Seaborn** | Sample datasets and statistical data visualization |
| **Scikit-learn** | Preprocessing, pipelines, classification, and model evaluation |
| **Jupyter Notebooks / Google Colab** | Interactive, reproducible experiments |
| **Git & GitHub** | Version control, progress tracking, and public documentation |

---

## Future Roadmap

This roadmap is a direction, not a claim that every topic has already been completed. It will be updated as new work is published.

- [x] **Data foundations:** inspect and clean a real-world-style dataset.
- [x] **Exploratory analysis:** investigate distributions, relationships, and correlations.
- [x] **Feature engineering:** encode categorical features for machine learning.
- [x] **Data preprocessing:** build a leakage-aware preprocessing workflow.
- [x] **Machine learning foundations:** train and evaluate baseline classifiers.
- [ ] **Statistical foundations:** deepen reasoning about distributions, sampling, and uncertainty.
- [ ] **Data engineering fundamentals:** design reliable ingestion, transformation, and storage workflows.
- [ ] **End-to-end projects:** connect analysis and engineering into documented, reproducible solutions.

---

## Working Principles

1. **Understand before automating.** Automation should make a sound process more reliable, not hide an unclear one.
2. **Preserve data integrity.** Every cleaning decision should have a reason and a traceable effect.
3. **Prefer clarity over cleverness.** Readable transformations are easier to review, test, and maintain.
4. **Make work reproducible.** Notebooks should communicate the steps, assumptions, and outcomes of an experiment.
5. **Learn in public.** Progress includes failed attempts, revised assumptions, and lessons learned — not just polished results.

---

## Follow the Journey

This repository will grow week by week as I connect my software engineering and automation experience with the principles of data science and data engineering.

**One week at a time. One experiment at a time. Always engineering with intention.**

---

*Maintained as a personal learning portfolio. Work in progress — continuously updated as the bootcamp advances.*
