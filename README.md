# Bank Loan Analysis Project

A concise, end-to-end exploratory and descriptive analysis of consumer bank loans for 2021. The analysis quantifies portfolio size, month-to-date (MTD) metrics, good vs. bad loan quality, and key drivers using Python and visualizations.

## Project Overview
- **Goal**: Analyze loan portfolio performance and trends to answer business questions such as volume, funding, repayments, and risk profile.
- **Scope**: Data profiling, portfolio KPIs, MTD metrics, cohort/monthly trends, and breakdowns by state, term, employment length, purpose, and home ownership.
- **Deliverable**: A single Jupyter notebook with visuals and computed metrics.

## Notebook
- File: `Bank Loan Project.ipynb`
- Core sections:
  - **Data load & profiling** (`df.info()`, `df.describe()`)
  - **Portfolio KPIs**: total funded amount, total amount received, averages (interest rate, DTI)
  - **MTD metrics**: applications, funded amount, amount received (based on latest `issue_date` month)
  - **Loan quality**: good loans (Fully Paid, Current) vs bad loans (Charged Off)
  - **Trends & visuals**:
    - Funded amount by month
    - Amount received by month
    - Loan applications by month
    - Funded amount by state
    - Funded amount by term (donut)
    - Funded amount by employment length
    - Funded amount by loan purpose
    - Funded amount by home ownership (treemap)

## Data
- Expected columns (24): `id`, `address_state`, `application_type`, `emp_length`, `emp_title`, `grade`, `home_ownership`, `issue_date`, `last_credit_pull_date`, `last_payment_date`, `loan_status`, `next_payment_date`, `member_id`, `purpose`, `sub_grade`, `term`, `verification_status`, `annual_income`, `dti`, `installment`, `int_rate`, `loan_amount`, `total_acc`, `total_payment`.
- Row count: ~38k (per current notebook run).

### Data file location
The notebook currently uses an absolute path to an Excel file via `pd.read_excel(...)`.
- Recommendation: place the dataset under `data/` and switch to a relative path, e.g. `data/financial_loan_data_excel.xlsx`.
- The dataset itself is not tracked in Git by default (see `.gitignore`).

## Key Metrics (from current run)
- **Total funded amount**: ~$435.76M
- **Total amount received**: ~$473.07M
- **Avg interest rate**: ~12.05%
- **Avg DTI**: ~13.33%
- **Good loan share**: ~86.18% (Fully Paid + Current)
- **Bad loan share**: ~13.82% (Charged Off)

## Environment & Requirements
Install dependencies from `requirements.txt` (Python 3.9+ recommended):

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## How to Run
1. Ensure the dataset is available locally. Recommended path: `data/financial_loan_data_excel.xlsx`.
2. Update the data path in the notebook if needed.
3. Launch Jupyter Lab/Notebook and run all cells:

```bash
jupyter lab
# or
jupyter notebook
```

## Repository Structure
```
Data Project/
├─ Bank Loan Project.ipynb          # Main analysis
├─ README.md                        # Project documentation
├─ requirements.txt                 # Python dependencies
├─ .gitignore                       # Ignore patterns (datasets, checkpoints, venv, etc.)
└─ data/                            # (Optional) dataset folder, ignored by Git
```

## Notes & Next Steps
- Replace absolute file paths with relative paths for portability.
- Consider exporting key tables/figures to `outputs/` and adding a lightweight HTML report.
- Add tests for metric calculations if evolving beyond EDA.

## License
Choose a license (e.g., MIT) if you plan to share or reuse. Add a `LICENSE` file.
