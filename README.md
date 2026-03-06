
# 🌍 Global Freelancers Dataset — Data Cleaning Report

## 📌 Project Overview
This project focuses on cleaning and standardizing a raw global freelancers dataset to improve data quality, consistency, and analytical usability.

The workbook contains two sheets:
- `global_freelancers_raw` → original, uncleaned dataset
- `global_freelancers(CLEANED)` → cleaned and analysis-ready dataset

All transformations were performed without removing any records.

## 🧹 Data Cleaning & Transformations
### 1️⃣ Name Standardization 
**What was done** 
* Split the original name column into:
  * first_name
  * last_name
  **Why**
  * Improves filtering, sorting, and individual-level analysis.
  * Removes ambiguity from titles and inconsistent naming formats.
  ---
