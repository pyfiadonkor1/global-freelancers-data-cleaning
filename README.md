
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
  * `first_name`
  * `last_name`
**Why**
  * Improves filtering, sorting, and individual-level analysis.
  * Removes ambiguity from titles and inconsistent naming formats.
    
  ---
### 2️⃣ Gender Normalization
**Before**
* Inconsistent values such as: `f`, `F`, `female`, `FEMALE`, `male`.
  
**After**
  * Standardized to:
    * `Male`
    * `Female`
    * 
**Impact**
 * Prevents duplicate categories during aggregation and visualization.

---
### 3️⃣ Activity Status Cleaning (`is_active`)
**Before**
* Mixed representations: `0`, `1`, `N`, and missing values
  
**After**
  * Converted to clear categorical values:
    * `Yes`
    * `No`
    * 
**Impact**
* Improves readability and supports direct filtering and grouping.

---
### 4️⃣ Hourly Rate (USD) Formatting
**Before**
* Stored as text with symbols and mixed formats (e.g., `$40`, `USD 100`)
  
**After**
 * Converted to numeric values (`float`) representing USD

**Impact**
* Enables accurate calculations such as averages, distributions, and comparisons.

---
### 5️⃣ Client Satisfaction Scaling 
**Before** 
* Values stored between `0` and `1` (e.g., `0.84`)
* Some missing values

**After** 
* Converted to percentage scale:
  * `0.84` → `84`
  * Missing values preserved
  
  **Impact**
  * More intuitive interpretation and better presentation in reports and dashboards.

 ---
 ### 6️⃣ Numerical Data Integrity
 The following columns were cleaned for consistency while preserving original values:

 * `age`
 * `years_of_experience`
 * `rating`

**Approach**
* No artificial imputation
* Missing values left unchanged to avoid bias
