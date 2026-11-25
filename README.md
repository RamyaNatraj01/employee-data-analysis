
# Employee Data Analysis

## Project Overview
This project focuses on analyzing employee data to understand employee attrition and identify factors that influence employees to leave an organization.

## Dataset
- Dataset Name: IBM HR Analytics Employee Attrition
- Source: Kaggle
- Format: CSV
- Total Records: 1470
- Total Columns: 35

## Technologies Used
- Python
- Pandas
- NumPy
- Jupyter Notebook
- Git
- GitHub

## Project Structure
```text
Employee-Data-Analysis/
│
├── data/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
│
├── notebooks/
│   └── employee_analysis.ipynb
│
└── README.md
```

## Initial Data Exploration
The following operations were performed:
1. Loaded the CSV dataset using Pandas.
2. Checked dataset shape.
3. Examined dataset information using info().
4. Generated statistical summary using describe().
5. Checked missing values using isna().sum().
6. Checked duplicate records using duplicated().sum().

## Business Questions
1. Which department has the highest employee attrition rate?
2. Does employee age have any relationship with employee attrition?
3. Does monthly income influence employee attrition?
4. Which job roles have the highest number of employees leaving the company?
5. Does years of experience at the company affect employee attrition?

## Project Objective
To identify employee attrition patterns and provide insights that can help organizations improve employee retention.
