
# Employee Data Analysis

## Project overview
This project explores employee data to identify patterns associated with employee attrition and to suggest areas for further retention analysis.

## Dataset
- Dataset: IBM HR Analytics Employee Attrition
- Format: CSV
- Records: 1,470
- Columns: 35
- Original data: `data/WA_Fn-UseC_-HR-Employee-Attrition.csv`

## Project structure
```text
employee-data-analysis/
├── data/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── notebooks/
│   ├── 01_data_overview.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_visualization.ipynb
│   ├── clean_data.csv
│   └── reports/
│       └── figures/
├── reports/
│   └── employee_data_analysis_report.html  # generated during report export
├── requirements.txt
└── README.md
```

The five chart images are currently saved in `notebooks/reports/figures/`, relative to the notebooks' working directory.

## Setup and run
Use Python 3 and run these commands from the repository root in PowerShell:

```powershell
py -m pip install -r requirements.txt
Set-Location notebooks
py -m jupyter notebook
```

Run the notebooks in order:
1. `01_data_overview.ipynb` reads the original CSV from `../data/`.
2. `02_data_cleaning.ipynb` creates `clean_data.csv`.
3. `03_exploratory_analysis.ipynb` and `04_visualization.ipynb` use `clean_data.csv`.

Run each notebook from the `notebooks/` directory so its relative data and figure paths resolve correctly.

## Report export
The visualization notebook contains the findings summary and charts. From the repository root, execute it and export the HTML report with:

```powershell
py -m jupyter nbconvert --to html --execute `
  --ExecutePreprocessor.cwd=notebooks `
  --ExecutePreprocessor.timeout=120 `
  --output-dir reports `
  --output employee_data_analysis_report.html `
  notebooks\04_visualization.ipynb
```

The generated report is `reports/employee_data_analysis_report.html`.

## Business questions
- How does attrition vary across departments and job roles?
- How are age, monthly income, and tenure associated with attrition?
- Which employee groups should be examined further as part of retention efforts?

## Limitations
This is a static sample dataset. The observed patterns describe associations and do not establish the causes of attrition or predict outcomes for other organizations.



