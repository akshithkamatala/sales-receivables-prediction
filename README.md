# Sales Receivables Management Analysis

This project combines **Alteryx** and **Python** to analyze and predict financial risk using real-world financial data.

---

## 🔧 Data Preparation in Alteryx

The Alteryx workflow overview:
1. Data Inputs
• Industry master data: Contains the company’s sector and industry information.
• Industry name-code mapping: Maps detailed industry names to industry codes.
• Financial statement data: Holds company financials like Revenues, Profit, and Accounts Receivables.
• Provisions and receivables aging data: Contains bad debt provisions and receivables aging breakdowns.
2. Data Preparation
• Fixing industry codes: Recode specific industry names like “Advertising” and “Market research”
to standardized codes.
• Updating marketing & leasing industries: Assign correct industry codes where needed.
• Converting dates: Parse text date fields into Date format for financial reports and provisions.
• Creating unique IDs: Combine company code and date into a single UID to enable proper joins
across datasets.
3. Joins
• Merge industry datasets: Combine industry master data with name-code mappings.
• Merge financial data with industry: Attach industry info to each company’s financial records.
• Merge provisions data: Bring in receivables and bad debt provision data to the financial dataset.
4. Data Filtering & Type Corrections
• Keep only records where:
– Financial year-end is Dec 31
– Revenue and Accounts Receivables are greater than 0.
• Convert all numeric fields to the correct decimal data types for analysis.
5. Metrics Calculations
• Prior Year AR: Pull prior year’s Accounts Receivables for each company.
• Average AR: Compute as an average of current and prior year AR.
• AR Turnover: Revenue ÷ Average AR.
• Bad Receivables Ratio: Provisions ÷ AR.
• Write-off Ratio: Write-offs ÷ AR.
6. Export
• Select only the finalized columns needed for analysis.
• Export the clean dataset as a CSV file ready for use in Python.
Outcome:
A clean, structured dataset containing key financials, industry info, and calculated receivables metrics across
31,433 of companies and multiple years, totaling to 227,000+ rows of data.
---

## 📊 Python Analysis

The Python notebook (`Sales_Receivable_Mgt_Analysis.ipynb`) includes:
- Exploratory and diagnostic analysis to understand relationships between receivables and financial strength
- Cluster-level comparisons of receivables intensity across industries
- A basic **OLS Regression** model using `statsmodels` and `sklearn` to predict `Provision_Bad_Receivables`

### 🔍 Key Insights:
- Weak correlations between profitability/cash flow and bad receivables provisions
- Technology & Media industries exhibit higher receivables intensity, suggesting greater reliance on credit sales
- The OLS model demonstrates basic predictive capability with interpretability (R² ≈ 0.14)

---

## 📁 Files

- [Alteryx Workflow Summary (PDF)](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/Alteryx_workflow_summary.pdf)
- [Alteryx Workflow Snapshot (PNG)](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/Workflow_snap.png)
- [Alteryx Workflow File (`.yxmd`)](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/data_cleaning.yxmd)
- [Python Analysis Notebook (`.ipynb`)](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/Sales_Receivable_Mgt_Analysis.ipynb)

---

## ✅ Tools Used

- **Alteryx** for data cleaning, transformation, and metric computation
- **Python**: `pandas`, `matplotlib`, `seaborn`, `statsmodels`, `sklearn`

---
