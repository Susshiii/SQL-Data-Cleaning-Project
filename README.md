# SQL-Data-Cleaning-Project
Cleaned and standardized messy layoff data using SQL (MySQL).

# 🧹 SQL Data Cleaning Project

## 📌 Overview
This project focuses on cleaning a real-world dataset containing layoff information. The data was taken from a GitHub resource provided in the **Alex The Analyst Bootcamp**.

## 🛠 Tools Used
- MySQL
- SQL (CTEs, UPDATE, TRIM, REPLACE, DELETE, ROW_NUMBER)

## 📂 Dataset
- Dataset: `layoffs.csv`
- Source: GitHub (via Alex The Analyst)

## ✅ Cleaning Steps Performed
1. **Removed duplicate records** using `ROW_NUMBER()` and CTEs.
2. **Standardized**:
   - Company names (`TRIM`)
   - Industry values (`LIKE` & `REPLACE`)
   - Country names (`TRIM`)
   - Date format using `STR_TO_DATE()`
3. Handled **NULL values** by either replacing or deleting based on context.
4. Dropped unnecessary columns (like `row_num`).

## 💡 Sample Query
```sql
UPDATE layoffs_staging2
SET company = TRIM(company);

