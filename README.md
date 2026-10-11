# Relational Databases — Homework 3

## Dataset

**Name:** Adult (Census Income)

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/2/adult)

**Dataset file:** [adult.data](https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data)

**Number of records:** 32,561

The dataset contains information about people's age, education, occupation, working hours, and other characteristics. The target variable indicates whether a person's annual income exceeds $50,000.

The complete `adult.data` file was used without sampling.

## Tools

- Google Colab
- PostgreSQL 16 (`pgserver`)
- Python
- SQLAlchemy
- pandas

## Homework Tasks

The following steps were completed:

1. **Data Loading** — Downloaded the dataset from UCI and imported it into PostgreSQL using `COPY FROM STDIN`.
2. **Data Cleaning** — Created staging and clean tables, converted data types, and replaced missing-value markers (`?`) with SQL `NULL`.
3. **Data Quality Audit** — Checked row counts, potential duplicates, missing values, and special markers.
4. **EDA** — Analyzed income distribution, working hours, and potential outliers.
5. **SQL Queries** — Executed 10 DQL queries using filtering, grouping, sorting, and other SQL operations.
6. **Reflection** — Summarized data-quality issues and possible use of the dataset for machine learning.

## Results

- 32,561 records loaded and cleaned.
- Missing values identified in `workclass`, `occupation`, and `native_country`.
- Income classes are imbalanced: approximately 76% earn $50K or less, and 24% earn more than $50K.
- The dataset is suitable for a binary classification task.

## How to Run

1. Open `hw3_adult.ipynb` in Google Colab.
2. Select **Runtime → Restart session and run all**.
3. Wait for all cells to complete.

The notebook automatically installs dependencies, downloads the dataset, creates PostgreSQL tables, and executes the SQL queries.

No manual dataset download or database setup is required.
