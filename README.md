# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analytics project that turns **3,900 retail transactions** into business insights, using **Python, PostgreSQL (SQL) and Power BI**.

!\[Dashboard Preview](dashboard/dashboard\_preview.png)

\---

## 📌 Project Overview

The goal is to understand how customers shop, what they spend on, and who is most valuable, so a business can make better decisions about subscriptions, discounts, products and marketing.

**Questions answered**

* Which customer groups (gender, age) bring in the most revenue?
* Which product categories and items perform best?
* How dependent are sales on discounts?
* Do subscribers spend more than non-subscribers?
* How loyal is the customer base?

\---

## 🗂️ Dataset

* **Rows:** 3,900 purchases
* **Columns:** 18
* **Includes:** customer demographics, item and category, purchase amount, season, size, colour, discount applied, previous purchases, purchase frequency, review rating, shipping type and subscription status
* **Source:** \[add the dataset link here, e.g. Kaggle]

\---

## 🔧 Tools Used

|Stage|Tools|
|-|-|
|Data cleaning and feature engineering|Python, pandas, Jupyter Notebook|
|Database and analysis|PostgreSQL, SQL, SQLAlchemy|
|Visualisation|Power BI|

\---

## 🔄 Workflow

1. **Data cleaning (Python)**

   * Inspected the data with `info()` and `describe()`
   * Filled 37 missing review ratings with the median rating of each product category
   * Renamed columns to snake\_case
   * Created new features: `age\_group` and `purchase\_frequency\_days`
   * Dropped `promo\_code\_used` because it duplicated `discount\_applied`
2. **Database integration**: loaded the cleaned DataFrame into PostgreSQL
3. **SQL analysis**: answered 10 business questions (see `sql/business\_queries.sql`)
4. **Dashboard (Power BI)**: built an interactive dashboard with slicers for subscription status, gender, category and shipping type

\---

## 📊 Key Insights

* **Male customers generate more revenue**: $157,890 vs $75,191 from female customers.
* **Younger customers lead**: Young Adults bring in $62,143, followed by Middle-aged ($59,197), Adults ($55,978) and Seniors ($55,763).
* **Clothing is the top category** by revenue (about $100K), followed by Accessories, Footwear and Outerwear.
* **Subscriptions are underused**: only **27%** of customers (1,053) are subscribers, but their average spend ($59.49) is almost the same as non-subscribers ($59.87). The opportunity is getting more people to subscribe.
* **Discounts matter for some products**: Hat (50%), Sneakers (49.7%) and Coat (49.1%) have the highest share of discounted purchases. 839 customers used a discount and still spent above the average purchase amount.
* **Express shipping** has a slightly higher average order value ($60.48 vs $58.46 for Standard).
* **Most customers are loyal**: 3,116 Loyal, 701 Returning and 83 New customers.
* **Top-rated products**: Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.78).

\---

## 💡 Business Recommendations

* **Boost subscriptions** by promoting exclusive subscriber benefits
* **Build loyalty programs** to reward repeat buyers
* **Review discount policy** to balance sales growth with profit margins
* **Promote top-rated and best-selling products** in campaigns
* **Target marketing** at high-revenue age groups and express-shipping users

\---

## 📁 Repository Structure

```
customer-behaviour-analysis/
├── README.md
├── data/
│   └── customer\_shopping\_behavior.csv
├── notebooks/
│   └── Customer\_Shopping\_Behaviour\_Analysis.ipynb
├── sql/
│   └── business\_queries.sql
├── dashboard/
│   ├── customer\_behaviour\_dashboard.pbix
│   └── dashboard\_preview.png
└── reports/
    ├── Customer\_Shopping\_Behavior\_Analysis.pdf
    └── Customer-shopping-behavior-decoded.pdf
```

\---

## 

