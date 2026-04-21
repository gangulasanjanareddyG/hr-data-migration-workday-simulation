# HR Data Migration — Workday Simulation

End-to-end HR data migration simulation built in Python.  
Demonstrates data profiling, transformation, and validation workflows similar to those used in enterprise systems like Workday.

---

## Project Summary

| Item | Detail |
|------|--------|
| Dataset | IBM HR Employee Attrition (1,470 records, 35 fields) |
| Tools | Python, Pandas, Jupyter Notebook |
| Output | Cleaned and validated Workday-style dataset |
| Validation Rules | 10/10 passed |

---

## Business Problem

When organizations migrate HR systems, poor data quality can lead to payroll errors, inconsistent employee records, and reporting issues.

This project simulates a typical migration workflow:
- Profile source data  
- Clean and transform it  
- Validate data before system load  

---

## Workflow Overview

### 1. Data Profiling
- Loaded HR dataset (1,470 records, 35 fields)  
- Checked for missing values and duplicates  
- Identified and removed non-informative constant columns  

---

### 2. Data Mapping & Cleaning
- Renamed fields to a standardized schema (Workday-style naming)  
- Standardized categorical values (e.g., Yes/No → 1/0, gender codes)  
- Cleaned inconsistencies and prepared structured dataset  
- Generated final dataset: `cleaned_hr_data.csv`  

---

### 3. Data Validation

Applied 10 data quality rules before migration:

| # | Rule | Result |
|---|------|--------|
| 1 | Row count = 1,470 | ✅ PASS |
| 2 | No null values | ✅ PASS |
| 3 | No duplicate worker IDs | ✅ PASS |
| 4 | Valid categorical values | ✅ PASS |
| 5 | Gender format valid | ✅ PASS |
| 6 | Travel codes valid | ✅ PASS |
| 7 | Age range valid | ✅ PASS |
| 8 | Salary > 0 | ✅ PASS |
| 9 | worker_status valid | ✅ PASS |
| 10 | Column structure correct | ✅ PASS |

All validation checks passed. Dataset is migration-ready.

---

## Key Skills Demonstrated

- Data Cleaning and Transformation  
- Data Quality Validation  
- Field Mapping  
- ETL Pipeline Concepts  
- Data Standardization  
- Basic Data Governance Practices  

---

## Folder Structure

    Data/
      raw_hr_data.csv
      cleaned_hr_data.csv

    Notebooks/
      01_data_profiling.ipynb
      02_mapping_cleaning.ipynb
      03_validation.ipynb

---

## How to Run

1. Clone this repository  
2. Download the dataset from Kaggle  
3. Place it in the `Data/` folder as `raw_hr_data.csv`  
4. Run notebooks in order:
   - 01_data_profiling  
   - 02_mapping_cleaning  
   - 03_validation  

---

## Dataset Source

[IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) (Kaggle)
