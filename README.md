# Data Science & Data Engineering Bootcamp
### An Engineering Journal — From Full-Stack Systems to Data-Driven Thinking

> **Build with purpose. Automate with intention. Treat data as a first-class engineering asset.**

Welcome to my **Data Science & Data Engineering Bootcamp** repository — a living record of my transition from building full-stack applications and intelligent automation systems to developing a deeper, more rigorous understanding of data.

My background is rooted in software engineering: designing application workflows, integrating APIs, building automation pipelines, and turning ideas into working products. That experience shaped the way I approach this new chapter. I don't see data science as a collection of notebooks or isolated algorithms; I see it as an engineering discipline that starts with trustworthy data, clear assumptions, reproducible workflows, and systems that solve real problems.

My philosophy is **automation-first, clean architecture, and data integrity**. I want every experiment to be understandable, every transformation to have a reason, and every result to be reproducible. This repository is where I document not only what I learn, but also the decisions, trade-offs, mistakes, and engineering lessons behind the work.

The goal is to build a practical portfolio that demonstrates steady progress — from data foundations and exploratory analysis toward reliable data workflows, machine learning, and data engineering practices.

---

## Repository Structure

The repository is organized chronologically by week. Each weekly folder will contain the notebooks, exercises, datasets or dataset references, and notes associated with that stage of the bootcamp.

```text
data-science-bootcamp/
│
├── week-01/
│   └── day3_titanic_cleaning.ipynb
│
├── week-02/
│   └── ...
│
├── week-03/
│   └── ...
│
├── week-04/
│   └── ...
│
└── README.md
```

> The structure will evolve as the bootcamp progresses. Future week folders will be added when their work is ready, rather than filled with empty or placeholder deliverables.

---

## Weekly Progress & Engineering Journey

### Week 01 — Foundations, Data Cleaning & Exploratory Data Analysis (EDA)

**Theme: Before asking data for answers, make sure it deserves your trust.**

The first stage of this journey is about building the habits that make downstream analysis meaningful. I started working with the classic **Titanic dataset** through Seaborn, using Pandas to inspect the data, understand its quality, and apply deliberate cleaning decisions.

This exercise may look simple at first: load a dataset, inspect missing values, and clean a few columns. But it introduces a fundamental engineering lesson — data preparation is not just a preprocessing chore. Every decision changes the dataset, and every change should be explainable.

#### Day 03 — Titanic Data Cleaning

**Notebook:** [day3_titanic_cleaning.ipynb](week-01/day3_titanic_cleaning.ipynb)

The workflow begins by loading the dataset and checking its dimensions and missing-value profile. From there, I focused on a few practical data-quality problems.

**1. Investigating missing data in `deck`**

The `deck` column has approximately **77% missing values** in the commonly used Seaborn Titanic dataset. Keeping a feature with that much missing information without a clear imputation strategy could introduce more uncertainty than value.

For this exercise, I removed the column rather than attempting to manufacture information for most of its records. The broader lesson is that missingness should be investigated before choosing between deletion, imputation, or a more advanced strategy.

**2. Choosing the median for `age`**

I filled missing ages using the column's **median**, rather than its mean.

The mean can be pulled toward unusually high or low observations. The median is more resistant to extreme values, making it a sensible baseline when a distribution is skewed or contains outliers. It is not automatically the right choice for every dataset, but it is a defensible choice here and keeps the initial cleaning workflow straightforward.

**3. Handling incomplete embarkation records**

Rows with missing values in `embarked` were removed using a targeted subset operation. This keeps the rule explicit: remove records missing this particular field, rather than dropping every row that contains any missing value across the dataset.

**4. Removing duplicate records**

I applied `drop_duplicates()` to remove exact duplicate rows. This is a useful baseline quality check, although real production pipelines should define what makes a record a duplicate according to the data's business keys and source semantics.

**5. Thinking critically about outliers with IQR**

The **Interquartile Range (IQR)** is a robust way to flag potential outliers without relying on the mean and standard deviation:

- `IQR = Q3 - Q1`
- Lower fence: `Q1 - 1.5 × IQR`
- Upper fence: `Q3 + 1.5 × IQR`

For numeric features such as `fare`, these fences can help identify unusually low or high observations for further investigation. An important distinction: an IQR flag is a signal to investigate, not an instruction to delete a record. Unusual values may be valid, meaningful observations. Outlier detection should therefore be driven by context and documented reasoning.

**Engineering note:** The current Day 03 notebook implements age imputation, removal of `deck`, targeted removal of rows missing `embarked`, duplicate removal, and a before/after missing-value check. The IQR section documents the outlier-analysis method; I will keep any implemented IQR filtering or deeper EDA clearly recorded in the notebook when that analysis is added.

#### What this week is teaching me

- Inspect first; transform second.
- Choose missing-value strategies based on the feature and its distribution.
- Prefer explicit, targeted transformations over broad deletion rules.
- Treat outliers as questions to investigate, not errors to erase automatically.
- Keep cleaning steps reproducible and explain why each one exists.

---

## Tech Stack & Tools

These are the core tools currently used or planned throughout the learning journey:

| Tool | Role in this repository |
|---|---|
| **Python** | Primary language for data analysis and engineering workflows |
| **Pandas** | Data loading, inspection, transformation, and cleaning |
| **Seaborn** | Sample datasets and statistical data visualization |
| **Scikit-learn** | Planned foundation for preprocessing and machine learning |
| **Jupyter Notebooks** | Interactive, reproducible experiments and technical notes |
| **Git & GitHub** | Version control, progress tracking, and portfolio publishing |

The stack will expand as new topics require additional tools. I will prioritize understanding the problem and the engineering trade-offs before adding complexity.

---

## Future Roadmap

This roadmap is a direction, not a claim that every topic has already been completed. I will update it as I work through each stage and publish the corresponding exercises.

- [x] **Week 01 — Data foundations and initial cleaning:** inspect the Titanic dataset, handle selected missing values, and remove duplicate rows.
- [ ] **Data exploration & visualization:** investigate distributions, relationships, correlations, and patterns through EDA.
- [ ] **Statistical foundations:** strengthen the ability to reason about distributions, variability, sampling, and uncertainty.
- [ ] **Data preprocessing:** explore encoding, scaling, feature preparation, and robust validation practices.
- [ ] **Machine learning foundations:** build and evaluate baseline models with Scikit-learn.
- [ ] **Data engineering fundamentals:** learn how to design reliable data ingestion, transformation, and storage workflows.
- [ ] **End-to-end projects:** connect analysis and engineering into documented, reproducible projects that solve practical problems.

---

## Working Principles

A few principles will guide how I build and document throughout this repository:

1. **Understand before automating.** Automation should make a sound process more reliable, not hide an unclear one.
2. **Preserve data integrity.** Every cleaning decision should have a reason and a traceable effect.
3. **Prefer clarity over cleverness.** Readable transformations are easier to review, test, and maintain.
4. **Make work reproducible.** Notebooks should communicate the steps, assumptions, and outcomes of an experiment.
5. **Learn in public.** Progress includes failed attempts, revised assumptions, and lessons learned — not just polished results.

---

## Follow the Journey

This repository will grow week by week as I connect my software engineering and automation experience with the principles of data science and data engineering.

I am building more than a collection of completed exercises. I am building the discipline to turn raw data into reliable insight — and, eventually, into dependable data-driven systems.

**One week at a time. One experiment at a time. Always engineering with intention.**

---

*Maintained as a personal learning portfolio. Work in progress — continuously updated as the bootcamp advances.*
