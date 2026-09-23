# data-cleaning-project
Data cleaning project # Dataset Cleaning README

## Dataset

Online Retail Transaction Dataset

## Cleaning Summary

The dataset was reviewed for data quality issues and cleaned to improve consistency and usability for analysis.

### 1. Missing Values

* **Description:** 1,454 missing values identified.

  * Replaced with `"Unknown"` where appropriate.
* **Customer ID:** 135,080 missing values identified.

  * Retained as NULL/blank because customer information was unavailable.

### 2. Duplicate Records

* Found **5,268 duplicate rows**.
* Removed all exact duplicate records.

### 3. Data Type Corrections

* **InvoiceDate** converted from text format to DateTime format.
* **Customer ID** converted from floating-point values to integer identifiers.

### 4. Standardization

* Trimmed leading and trailing spaces from text fields.
* Standardized **Country** values for consistent capitalization.
* Standardized **Description** values to a consistent text format.

## Result

The cleaned dataset:

* Contains no duplicate records.
* Uses appropriate data types for dates and identifiers.
* Has standardized text values.
* Is ready for further analysis in Excel, SQL, Python, Power BI, or machine learning workflows.

## Files

* `DATA CLEANING.csv` – Original dataset
* `Cleaned_Data.csv` – Cleaned dataset

