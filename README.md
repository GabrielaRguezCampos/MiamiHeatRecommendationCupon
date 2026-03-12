# 🏀 Sports Venue Market Basket Analysis
### Miami Heat — Concessions & Retail Analytics
*Enterprise analytics project developed during my role as Data Analytics Associate at the Miami Heat (NBA)*

---

## ⚠️ Confidentiality Notice

This repository contains a **sanitized overview** of an analytics project developed using proprietary transactional data. Raw data, venue-specific outputs, client dashboards, and internal business metrics are not included in this repository in compliance with confidentiality obligations.

---

## Project Overview

Developed an end-to-end market basket analysis pipeline to identify product affinity patterns in concessions and retail transactions at a major NBA venue. Findings were used to drive **pricing strategy, product bundling, and promotional recommendations** presented directly to business stakeholders.

---

## Objectives

- Identify frequently co-purchased item combinations across thousands of transactions
- Quantify association strength using support, confidence, and lift metrics
- Surface actionable bundling and upsell opportunities by product category
- Deliver findings in a format accessible to non-technical business stakeholders

---

## Methods & Techniques

| Method | Purpose |
|---|---|
| Apriori Algorithm | Association rule mining on transaction data |
| Support / Confidence / Lift | Rule evaluation and filtering |
| Exploratory Data Analysis | Transaction volume, basket size, category distribution |
| Data Cleaning & Preprocessing | Handling nulls, encoding, transaction formatting |
| Visualization | Heatmaps, bar charts, network graphs of item associations |

---

## Tech Stack

```
Python · Pandas · mlxtend · Matplotlib · Seaborn · Jupyter Notebook
```

---

## Sample Methodology (Sanitized)

```python
from mlxtend.frequent_patterns import apriori, association_rules
from mlxtend.preprocessing import TransactionEncoder
import pandas as pd

# Encode transactions into binary matrix
te = TransactionEncoder()
te_array = te.fit_transform(transactions)
df = pd.DataFrame(te_array, columns=te.columns_)

# Mine frequent itemsets
frequent_itemsets = apriori(df, min_support=0.01, use_colnames=True)

# Generate association rules
rules = association_rules(frequent_itemsets, metric="lift", min_threshold=1.2)
rules_sorted = rules.sort_values("lift", ascending=False)
```

---

## Key Outcomes

- Identified high-lift item pairings that informed combo meal and bundle design
- Provided category-level affinity insights across multiple venue sections
- Recommendations presented to operations and F&B business stakeholders
- Analysis contributed to pricing strategy discussions for upcoming event seasons

---

## What I Can't Share

In compliance with my employment agreement and data confidentiality obligations, the following are **not included** in this repository:

- Raw or processed transactional data
- Venue-specific product names, pricing, or revenue figures
- Internal dashboards or Power BI reports
- Client-facing deliverables or presentation materials

---

## Related Public Work

For a fully documented version of association rule mining on open data, see:  
👉 [FIFA World Cup Venue Market Basket Analysis](https://github.com/GabrielaRguezCampos/market-basket-analysis-sports-venue)  
*(Same methodology applied to a publicly available dataset)*

---

## Author

**Gabriela Rodriguez** · Data Analytics Associate, Miami Heat  
[LinkedIn](https://www.linkedin.com/in/gabriela-rodriguez) · [GitHub](https://github.com/GabrielaRguezCampos)
