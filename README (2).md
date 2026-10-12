# Olist E-Commerce Sales & Customer Analytics

## Project Overview

This project explores the Brazilian E-Commerce Public Dataset by Olist to examine sales performance, product categories, geographic revenue distribution, delivery performance, and customer review scores. The work combines exploratory data analysis in JupyterLab with a Power BI dashboard designed to communicate business findings clearly.

## Objectives

- Track product revenue over time.
- Identify product categories and states contributing the most revenue.
- Examine delivery timeliness and its relationship with customer review scores.
- Present the main findings in a concise, business-oriented Power BI report.

## Tools and Libraries

**Analysis environment**
- **JupyterLab** — notebook environment used to run and document the analysis.
- **Python** — programming language used in the notebook.

**Python libraries imported in the project notebook**
- **pandas** — loading, cleaning, transforming, and summarizing tabular data.
- **NumPy** — numerical operations.
- **Matplotlib** — creating charts.
- **Seaborn** — statistical data visualization.
- **pathlib** (Python standard library) — handling file paths.

**Reporting**
- **Power BI Desktop** — building the interactive report and KPI cards.
- **GitHub** — versioning and presenting the project as a portfolio.

## Dashboard

### Page 1 — Sales Overview

- **Total Revenue:** approximately R$13.22 million
- **Delivered Orders:** approximately 96K
- Monthly E-Commerce Revenue
- Top 10 Product Categories by Revenue
- Top 10 States by Revenue

### Page 2 — Delivery & Customer Satisfaction

- Customer Satisfaction: On-Time vs. Late Delivery
- Review-score comparison for on-time and late deliveries

## Selected Findings

- Product revenue in the prepared delivered-order analysis was approximately **R$13.22 million**.
- The analysis included **96,478 delivered orders**.
- **Health & Beauty** was the highest-revenue category in the prepared category summary.
- **São Paulo (SP)** generated the highest revenue among the states shown.
- Late deliveries had a lower average review score than on-time deliveries in the prepared analysis.
- Repeat purchasing was relatively low in the analyzed delivered-order sample, suggesting a possible customer-retention opportunity.

*Interpretation note:* These are descriptive findings from the prepared dataset and depend on the filters, join logic, order statuses, and aggregation methods used. The revenue KPI refers to product revenue in this analysis and should not be interpreted as total platform revenue inclusive of all fees.

## Data Preparation and Outputs

The analysis notebook loads the Olist customer, order, order-item, payment, review, product, and product-category translation tables, then creates summary CSV files used in Power BI. Summary outputs used in the dashboard include:

- `monthly_sales_summary`
- `category_performance`
- `state_performance`
- `delivery_review_summary`

Care is needed when joining tables with different levels of detail. Duplicate rows and one-to-many relationships can inflate totals if the data are not aggregated at the correct grain.

## Repository Contents

The exact file names and folders should match the repository. The project package was organized around this structure:

```text
olist_ecommerce_portfolio/
├── data/                           # Olist source CSV files
├── notebooks/
│   └── ecommerce_analysis.ipynb    # JupyterLab analysis notebook
├── summaries/                      # Exported summary CSV files
├── visualizations/                 # Exported charts, if included
├── requirements.txt                # Python library dependencies
├── Olist_Ecommerce_Dashboard.pbix  # Power BI report (use your actual filename)
└── README.md
```

## Reproducing the Analysis

1. Download the Olist dataset from its original source and place the CSV files in the project's data folder.
2. Open `notebooks/ecommerce_analysis.ipynb` in JupyterLab.
3. Install the libraries listed in `requirements.txt` if they are not already available.
4. Run the notebook cells to load, prepare, analyze, and export the summary CSV files.
5. Open the Power BI `.pbix` report in Power BI Desktop. If prompted, update the data-source paths to the locations on your computer.

## Limitations

- Results depend on data preparation choices, join keys, order-status filters, and aggregation logic.
- The analysis is descriptive and does not establish that delivery delays cause lower customer ratings.
- Recheck headline figures against the final notebook outputs before using them in a formal business report.

## Author

A data analytics portfolio project demonstrating data preparation, exploratory analysis, visualization, and business intelligence reporting.
