
# Sales Receivables Management Analysis

This project combines **Alteryx** and **Python** to analyze and predict financial risk using real-world financial data.

---

## 🔧 Step 1: Data Preparation in Alteryx

The Alteryx workflow handles:
- Merging industry classification and name mappings
- Filtering financial records to include only those with meaningful Receivables and Revenues
- Computing custom metrics such as AR Turnover, Bad Receivables Ratio, and Write-offs
- Preparing the final clean dataset for export to CSV

![Detailed Alteryx Summary](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/Alteryx_workflow_summary.pdf)

![Alteryx Workflow](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/data_cleaning.yxmd)

![Alteryx Workflow_Snap](https://github.com/akshithkamatala/sales-receivables-prediction/blob/main/Workflow_snap.png)

---

## 🐍 Step 2: Python Analysis

The Python notebook (`Sales_Receivable_Mgt_Analysis.ipynb`) performs:
- Exploratory and diagnostic analysis to understand relationships between receivables and financial strength
- Cluster-level comparisons of receivables intensity
- A basic **OLS Regression** model using `statsmodels` and `sklearn` to predict `Provision_Bad_Receivables`

Key insights include:
- Weak correlations between profit/cash flow and bad receivables
- Technology & Media firms carry higher receivables intensity, indicating reliance on credit sales
- The OLS model gives basic predictive capability with interpretability (R² ≈ 0.14)

---

## 📁 Files

- `Sales_Receivable_Mgt_Analysis.ipynb` — Full Python notebook for analysis
- `Alteryx_Workflow.png` — Visual of the preprocessing steps in Alteryx

---

## ✅ Tools Used

- **Alteryx** for data cleaning, merging, and metric computation
- **Python** (`pandas`, `matplotlib`, `seaborn`, `statsmodels`, `sklearn`) for analysis and modeling

---

This project is ideal to demonstrate:
- End-to-end business analyst skills: data wrangling, visualization, and basic modeling
- Proficiency in combining tools like Alteryx and Python
