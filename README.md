# Edu Project — Online Learning Platform EDA

This repo contains a small exploratory data analysis (EDA) notebook for an online education platform dataset.

## Project description

This project explores an online education platform dataset to understand learner demographics and enrollment behavior. Using Python (pandas, matplotlib, seaborn), it loads the **Users**, **Courses**, and **Transactions** sheets from an Excel workbook, performs basic cleaning and feature engineering (including `AgeGroup`), and merges the tables into a single analysis dataset. The notebook then summarizes key counts (such as total enrollments) and visualizes patterns by age group, gender, course category, and course level, including a heatmap showing how course interests vary across age segments.

## What’s inside

- **Notebook:** `-1.ipynb`
- **Dataset:** `EduPro_Online_Platform_Dataset.xlsx`

The notebook:
- Loads 3 sheets (**Users**, **Courses**, **Transactions**) from the Excel file
- Cleans a few fields (age filtering, gender capitalization, transaction date parsing)
- Builds an `AgeGroup` feature
- Merges the three tables into a single analysis dataframe
- Produces summary metrics and plots (bar charts, pie chart, and a heatmap)

## Requirements

- Python 3.9+ recommended
- Jupyter (VS Code notebooks or JupyterLab)
- Python packages:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `openpyxl` (required by `pandas.read_excel` for `.xlsx`)

If you want to install everything in one go:

```bash
pip install -r requirements.txt
```

## Quickstart

1. (Optional) Create and activate a virtual environment

```bash
python -m venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Open and run the notebook

- Open `Untitled-1.ipynb` in VS Code.
- Select the `.venv` kernel.
- Run cells from top to bottom.

## Dataset expectations

The notebook expects the Excel file `EduPro_Online_Platform_Dataset.xlsx` in the same folder as the notebook.

It references these columns (minimum required):

- **Users** sheet: `UserID`, `Age`, `Gender`
- **Courses** sheet: `CourseID`, `CourseCategory`, `CourseLevel`
- **Transactions** sheet: `UserID`, `CourseID`, `TransactionDate`

## Outputs

Running the notebook generates:

- Total enrollments (row count of merged dataset)
- Enrollments by age group (bar chart)
- Gender distribution (pie chart)
- Course category popularity (bar chart)
- Course level preference (bar chart)
- Age group vs course category (heatmap)

## Notes

- Age is filtered to keep users with ages between 10 and 70.
- `AgeGroup` bins are: `<18`, `18–25`, `26–35`, `36–45`, `45+`.
