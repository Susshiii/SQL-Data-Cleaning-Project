# 🧠 SQL Data Cleaning + EDA Project – Layoffs Dataset

## 📌 Overview
This project demonstrates a full SQL-based workflow: starting with cleaning a messy layoffs dataset and ending with extracting key insights using exploratory data analysis (EDA). The dataset was provided in the [Alex The Analyst Bootcamp](https://www.youtube.com/@AlexTheAnalyst).

## 🛠 Tools Used
- MySQL
- SQL (CTEs, Window Functions, DATE formatting, Aggregations)

## 📂 Dataset
- Dataset: `layoffs.csv`
- Source: GitHub via Alex The Analyst's course

---

## 🔹 Part 1: Data Cleaning

### ✅ Steps Performed:
- Created a staging table to protect the original dataset
- Removed duplicates using `ROW_NUMBER()`
- Standardized:
  - Company names (e.g., `TRIM(company)`)
  - Industries (e.g., fixing `"Crypto "` → `"Crypto"`)
  - Country names and Date formats
- Handled missing/null values
- Dropped unnecessary columns

### 🧾 Sample Query:
```sql
UPDATE layoffs_staging2
SET industry = 'Crypto'
WHERE industry LIKE 'Crypto%';
