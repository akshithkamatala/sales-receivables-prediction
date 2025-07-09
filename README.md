# sales-receivables-prediction
Predicting bad debt provisions using regression models on financial receivables data (31,000+ companies).


“This project analyzes financial statement data to assess the receivables management efficiency, aging risk, and bad debt practices across industries. It focuses on understanding how these factors vary over time and between sectors, ultimately guiding predictive and prescriptive insights on financial health and receivables risk.”



Overall Python Analysis Plan
STEP 1: Setup & Data Load
Import the CSV from Alteryx.

Do a quick data sanity check (shapes, column types, nulls).

Explore data distributions.

STEP 2: Outliers & Anomaly Detection 🔎
Before doing analysis:

Visualize outliers (Boxplots, Histograms).

Detect unusual AR turnover or bad debt ratios using:

IQR Method

Z-score / Modified Z-score

Isolation Forest (optional)

We’ll flag anomalies but won’t remove them unless they are clearly data errors.

STEP 3: Descriptive Analysis 🟦
Summary stats by industry, year.

Key trends in:

Revenues

Accounts Receivables

AR Turnover

Bad Receivables & Write-off Ratios.

STEP 4: Diagnostic Analysis 🔬
Correlation analysis (heatmaps).

How do bad debt ratios correlate with revenues or AR turnover?

Are some industries consistently underperforming?

Year-over-year comparisons for companies with >2 years of data.

STEP 5: Predictive Analysis 📈
Build a simple regression model:

Target: Bad_Receivables_Ratio or Writeoff_Ratio.

Features: Revenues, AR, AR Turnover, Industry.

See what variables explain bad debt practices.

(Optional):

Time series forecast for individual companies' AR or Revenue.

STEP 6: Prescriptive Insights 🧑‍💼
Recommend industries that should review their AR or bad debt policies.

Suggest AR Turnover benchmarks.
