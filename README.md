## Retail Sales Analysis — Exploratory Data Analysis

Exploratory analysis of 5,000 retail transactions, looking at what actually drives revenue, which segments and categories perform best, and what the data can and can't tell you about it.

#### Overview

This project analyzes a synthetic retail sales dataset (5,000 transactions, 14 variables) following a standard EDA workflow:

**Data Quality → Exploration → KPI Analysis → Segmentation → Trend Analysis → Relationship Analysis → Business Interpretation**


#### Business Questions

1. Which product categories generate the most revenue and sales volume?
2. Which customer age groups contribute the most transactions and revenue?
3. How is revenue distributed across the available time period?
4. Which payment methods are most frequently used?
5. How do unit price, quantity, discount, age, delivery time, and customer rating relate to revenue?
6. What's missing here that would be needed before any of this becomes a real business decision?

#### Dataset
The dataset's dates run from 2022 to 2035, which obviously isn't real history. So the trend analysis here is meant to show the method, not actual seasonality.

Before analysis, I checked the data for structure, dtypes, missing values, duplicates, date formatting, and numeric ranges, then saved the cleaned version separately from the raw file.

#### Key Findings

**Product performance.** Electronics led both metrics: 7,109 units sold and about ₹1.83M in revenue, ahead of Clothing (6,171 units, ~₹1.53M), Home (~₹982K), and Beauty (~₹766K). It's the obvious place to look first if you were reviewing inventory or category investment, but revenue alone doesn't tell you if it's actually profitable. That needs margin, stock, and returns data this dataset doesn't have.

**Customer segments.** Customers aged 26–35 have both the highest transaction count and the highest revenue, at roughly ₹1.32M. That makes them the largest segment here, but not necessarily the most valuable one. Whether they buy more often, spend more per order, or come back is a separate question that would need purchase-history data this dataset doesn't include.

**Payment behavior.** Card is the most-used method (2,270 transactions) and brings in the most revenue (~₹2.37M), ahead of COD and Wallet. Looking at revenue and AOV alongside the transaction count gives a fuller picture than transaction count on its own.

**Revenue drivers.** Unit price (0.68) and quantity (0.62) correlate most strongly with revenue; discount is weakly negative (-0.14). Age, delivery days, and customer rating barely move the needle. Worth flagging: revenue is literally calculated from quantity, price, and discount, so part of this correlation is just how the metric is built, not a discovery about customer behavior. None of this proves that changing price or quantity would increase revenue.

#### KPIs Used

Total Revenue · Total Transactions · Total Units Sold · Average Order Value (AOV) · Average Units per Transaction · Average Discount · Average Customer Rating · Average Delivery Days

AOV specifically was included to separate "more orders" from "bigger orders," since revenue alone can't tell the two apart.

#### Limitations

- Synthetic dataset, not real market history.
- No cost or margin data, so revenue findings can't be turned into profitability findings.
- No customer ID or purchase history, so retention and lifetime value aren't measurable.
- Category-level only, no product-level detail.
- No marketing spend or inventory data to explain demand.
- Correlation results show association, not causation.

#### Next Steps

To take this further, I'd want product cost and margin data, customer purchase history, marketing spend and conversions, and inventory/stock-out records. That's what would move this from "here's what happened" to "here's what to do about it."

#### Tools & Skills

**Tools:** Excel, Python, Pandas, Matplotlib, Seaborn, Jupyter Notebook

**Skills demonstrated:** data cleaning, data wrangling, EDA, KPI design, descriptive statisitics, customer and product segmentation, correlation analysis, graphs and chart visualizations, and business interpretation, including being upfront about where a finding stops and a real decision would need more data.

#### Takeaway

"Electronics generated the highest revenue" is a finding. "What's driving that, and is it actually profitable?" is the next question, and answering it needs data this dataset doesn't have. That distinction, between what the data shows and what you can actually decide from it, is what I tried to keep front and center throughout this analysis.

#### Author

**Zubia Ansari** —  Data & BI Analyst
[LinkedIn](https://www.linkedin.com/in/zubia-ansari01/) · [GitHub](https://github.com/ansarizubia)