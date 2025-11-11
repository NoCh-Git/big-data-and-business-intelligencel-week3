# Session 2 — Big Data and Business Intelligence

This repository contains the materials for **Session 2** of *Big Data and Business Intelligence*.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---

## Session Outline

This session focuses on **Feature Engineering and Data Preparation for BI**, covering the complete pipeline from raw messy data to dashboard-ready datasets.

### Learning Objectives
- Understand data quality issues in real-world business data
- Apply systematic cleaning strategies (standardization, imputation, validation)
- Distinguish between technical validation and business rules
- Design metrics and KPIs for dashboards
- Create production-ready datasets for BI tools

### Notebooks

1. **[1_Big_Data_and_BI_data_profiling.ipynb](./notebooks/1_Big_Data_and_BI_data_profiling.ipynb)**
   - Data quality audit and profiling
   - Identifying missing values, inconsistent categories, and data issues
   - Defining a concrete cleaning plan based on business requirements
   - Determining critical columns for dashboards

2. **[2_Big_Data_and_BI_imputation_and_standardization.ipynb](./notebooks/2_Big_Data_and_BI_imputation_and_standardization.ipynb)**
   - Parsing mixed date formats
   - Standardizing categorical values (country, channel)
   - Imputation strategies for missing data (median, constant, unique placeholders)
   - Handling primary keys with unique high-value IDs
   - Creating cleaned columns for downstream analysis

3. **[3_Big_Data_and_BI_data_integrity_and_outliers.ipynb](./notebooks/3_Big_Data_and_BI_data_integrity_and_outliers.ipynb)**
   - Technical validation vs. business rules
   - Implementing sanity checks (date, quantity, price validation)
   - Applying business rules from stakeholder requirements
   - Fixing data quality issues (negative quantities)
   - Calculating revenue with validated data

4. **[4_Big_Data_and_BI_metric_design_on_demand.ipynb](./notebooks/4_Big_Data_and_BI_metric_design_on_demand.ipynb)**
   - Designing KPIs without bloating tables
   - Revenue and discount calculations
   - Aggregating metrics for dashboards (by country, channel)
   - Understanding semantic/model layer concepts

5. **[5_Big_Data_and_BI_dashboard_dataset.ipynb](./notebooks/5_Big_Data_and_BI_dashboard_dataset.ipynb)**
   - Combining all cleaning steps into a complete pipeline
   - Deciding when to keep vs. drop columns
   - Final validation and quality checks
   - Exporting dashboard-ready CSV for BI tools
   - Documentation and data lineage

### Key Concepts Covered
- **Data Profiling**: Systematic audit of data quality issues
- **Imputation**: Median vs. mean, constant values, unique placeholders
- **Standardization**: Lowercase, strip, dictionary mapping
- **Validation**: Technical sanity checks vs. domain-specific business rules
- **Primary Key Preservation**: Using high-value unique IDs for missing values
- **Metric Design**: On-demand calculation vs. pre-computed columns
- **Production Best Practices**: SQL-safe IDs, dynamic calculations, documentation

---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
