# Sales Receivables Management Analysis

This project combines **Alteryx** and **Python** to analyze and predict financial risk using real-world financial data.

---

## 🔧 Data Preparation in Alteryx

The Alteryx workflow performs:
- Merging industry classification and name mappings
- Filtering financial records to include only those with meaningful Receivables and Revenues
- Computing custom metrics such as AR Turnover, Bad Receivables Ratio, and Write-off Ratio
- Exporting the final cleaned dataset to CSV for analysis in Python

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
