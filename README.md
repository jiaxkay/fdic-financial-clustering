# FDIC Bank Data Analysis and Clustering

This project analyzes **U.S. bank financial data** using the **FDIC Public API**, combining data retrieval, feature engineering, exploratory data analysis (EDA), and unsupervised learning to uncover patterns in capital structure and commercial real estate (CRE) exposure.

---

## Project Summary
- **Goal:** Identify financial patterns and risk groupings among U.S. banks  
- **Data Source:** [FDIC Public API](https://banks.data.fdic.gov/docs/)  
- **Core Techniques:**  
  - Data aggregation and feature engineering  
  - Exploratory Data Analysis (EDA)  
  - **Principal Component Analysis (PCA)** for dimensionality reduction  
  - **KMeans Clustering** for segmentation  
  - Visualization of CRE concentration, historical trends, and PCA clusters  

---

## Requirements

- pandas
- numpy
- requests
- matplotlib
- seaborn
- scikit-learn
- scipy

Install via:
```bash
pip install -r requirements.txt
```
## Workflow Overview

- Data Retrieval — fetch institutional and financial reports through FDIC APIs

- Aggregation & Feature Engineering — compute ratios like CRE / Asset, Equity / Asset, Tier1 / RWA, etc.

- EDA & Visualization — scatterplots, boxplots, and trend lines to reveal bank size and CRE exposure

- Dimensionality Reduction (PCA) — compress correlated variables into interpretable components

- Clustering (KMeans) — group banks with similar capital and loan characteristics

- Interpretation — visualize clusters and examine differences by asset class (Small, Medium, Large)

---

## Key Outputs

- CRE Ratio vs. Asset Size (2024) — distribution of CRE exposure by bank scale

- Historical CRE Trends (2015–2024) — average CRE ratio evolution

- CRE Portfolio Composition — stacked bar chart by loan type and asset class

- PCA + KMeans Plot — visualization of capital structure clusters

---

## How to Run

- Place the institutions_definitions.csv and All Financial Reports.xlsx in your project folder

- Update the project_folder path in the script if needed

- Run the Python script or open the Jupyter notebook version:

```bash
python fdic_analysis.py
```

---

## Example Insights

- **CRE Ratio:** Small banks have higher CRE exposure; large banks have lower CRE exposure.  
- **Historical Trend (2015–2024):** CRE ratio grew from 2015–2019, declined from 2019–2021, then accelerated after 2021.  
- **CRE Portfolio Composition:**  
  - Large banks: more Multifamily Residential loans  
  - Small banks: more Owner-Occupied CRE loans  
  - All banks: Commercial RE Other dominates across asset classes  
- **PCA + KMeans Clusters:**  
  - **Cluster 0:** Medium banks, moderate capital, moderate risk  
  - **Cluster 1:** Small banks, stronger capital, slightly lower risk (conservative type)  
  - **Cluster 2:** Small banks, higher CRE ratio and higher risk (aggressive type)  
- **Key Observation:** Small banks show a **two-extreme pattern** — either conservative (Cluster 1) or aggressive (Cluster 2), medium banks are mostly moderate (Cluster 0), and large banks are evenly distributed across clusters, showing more stable and diversified behavior.


---

## Author

**Kay J**  
Boston, MA  
Business & Data Analyst — Python | SQL | Power BI | Financial Data Modeling


