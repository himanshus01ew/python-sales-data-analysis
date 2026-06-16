# 🛒 E-Commerce Sales Analysis — Python Capstone Project

An end-to-end data analytics project using an Indian e-commerce dataset (2022–2024). This notebook walks through a complete real-world analytics workflow: data loading, cleaning, exploration, visualisation, and business insight extraction.

---

## 📋 Project Overview

**Dataset:** `ecommerce_sales.csv` — Indian e-commerce orders from 2022 to 2024  
**Notebook:** `python_project.ipynb`

### Topics Covered

| Module | Focus Area | Key Skills |
|--------|-----------|------------|
| 1 | Setup & Data Loading | File I/O, pandas basics |
| 2 | Data Inspection | dtypes, shape, missing values |
| 3 | Data Cleaning | Type casting, deduplication, derived columns |
| 4 | Python Core & Intermediate | List comprehensions, lambda, map/filter, OOP |
| 5 | NumPy | Arrays, vectorised ops, descriptive stats |
| 6 | Pandas EDA | GroupBy, pivot tables, string operations |
| 7 | Matplotlib | Line, bar, pie, scatter, subplots |
| 8 | Seaborn | Heatmap, boxplot, violin, pairplot |
| 9 | Business Insights | KPIs, customer segmentation, YoY growth |
| 10 | GitHub | Git workflow & deployment |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Notebook

```bash
jupyter notebook python_project.ipynb
```

---

## 📂 Project Structure

```
ecommerce-capstone/
├── python_project.ipynb   # Main analysis notebook
├── ecommerce_sales.csv    # Dataset
├── README.md              # This file
├── .gitignore
└── plots/                 # Generated visualisation outputs
    ├── plot_monthly_trend.png
    ├── plot_category_revenue.png
    ├── plot_payment_pie.png
    ├── plot_scatter.png
    ├── plot_dashboard.png
    ├── plot_heatmap.png
    ├── plot_boxplot.png
    ├── plot_violin.png
    ├── plot_monthly_heatmap.png
    ├── plot_pairplot.png
    └── plot_yoy_growth.png
```

---

## 📊 Key Analyses

### Data Cleaning
- Parsed `order_date` into datetime and extracted year, month, quarter, and day-of-week columns
- Imputed missing `customer_age` with median; filled missing `customer_gender` and `discount_pct`
- Removed duplicate `order_id` entries and validated numeric column ranges

### Python Core & OOP
- Classified customers into age groups using list comprehensions
- Assigned revenue tiers (`High / Medium / Low`) via lambda + `map()`
- Built an `OrderAnalytics` class encapsulating total revenue, average order value, top categories, and delivery rate

### NumPy
- Vectorised revenue recalculation (`price × qty × (1 − discount)`) and verified against stored totals
- Computed descriptive statistics (mean, median, std, IQR, percentiles)
- Identified top-10% orders by revenue using boolean masking

### Pandas EDA
- GroupBy aggregations: revenue, order count, average discount, and rating by category
- Pivot tables: revenue by category × year; payment method usage by city
- String operations on product names

### Visualisations (Matplotlib & Seaborn)
- Monthly revenue trend line chart
- Category revenue horizontal bar chart
- Payment method pie chart
- Unit price vs. total price scatter (log scale)
- 2×2 dashboard: order status donut, orders by weekday, age histogram, top-5 cities by revenue
- Correlation heatmap, boxplot and violin plot by category, monthly revenue heatmap, pairplot

### Business KPIs
- Delivery rate, total revenue, average order value, average rating, return rate
- Customer segment analysis by age group
- Top 10 products by revenue
- Year-over-year category revenue growth (2022 → 2024)

---

## 🔧 Dataset Columns

| Column | Description |
|--------|-------------|
| `order_id` | Unique order identifier |
| `order_date` | Date of order placement |
| `customer_id` | Unique customer identifier |
| `customer_age` | Customer age |
| `customer_gender` | Customer gender |
| `customer_city` | City of the customer |
| `category` | Product category |
| `product_name` | Name of the product |
| `unit_price` | Price per unit (₹) |
| `quantity` | Number of units ordered |
| `discount_pct` | Discount applied (%) |
| `total_price` | Final order value (₹) |
| `payment_method` | Payment method used |
| `order_status` | Delivered / Returned / Cancelled / Pending |
| `rating` | Customer rating (1–5) |

---
