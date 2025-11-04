# customer-shopping-behavior-analysis
End-to-end analysis of customer shopping behavior using Python (Pandas) for cleaning, PostgreSQL for SQL insights, and Power BI for visualization.

# Customer Shopping Behavior Analysis Portfolio Project

[cite_start]This project performs an end-to-end analysis of customer shopping behavior based on 3,900 transactional records[cite: 3]. [cite_start]The goal is to uncover actionable insights into spending patterns, customer segments, product preferences, and subscription behavior to inform strategic business decisions[cite: 4, 110, 111].

[cite_start] [cite: 67]

---

## 🛠️ Technology Stack

This analysis was conducted using the following tools:

* [cite_start]**Python (Pandas):** For data loading, cleaning, preprocessing, and feature engineering[cite: 14, 21].
* [cite_start]**PostgreSQL (SQL):** For in-depth data analysis and answering key business questions by querying the cleaned data[cite: 26, 27].
* [cite_start]**Power BI:** For creating a final interactive dashboard to visualize the findings[cite: 62, 63].

---

## ⚙️ Project Workflow

The project followed a structured data analysis process:

1.  **Data Cleaning (Python):**
    * [cite_start]Loaded the dataset (3,900 rows, 18 columns) into a pandas DataFrame[cite: 6, 7, 15].
    * [cite_start]Handled 37 missing `Review Rating` values by imputing the median rating for each product's category[cite: 12, 19, 128].
    * [cite_start]Standardized column names to `snake_case` for better readability and SQL compatibility[cite: 20, 134].

2.  **Feature Engineering (Python):**
    * [cite_start]Created a new `age_group` column by binning customer ages[cite: 22, 131].
    * [cite_start]Checked for data redundancy and dropped the `promo_code_used` column, as `discount_applied` captured the necessary information[cite: 24, 135].

3.  **Database Integration:**
    * [cite_start]Loaded the cleaned and transformed DataFrame into a PostgreSQL database for structured querying[cite: 25, 138].

4.  **SQL Analysis:**
    * Wrote 10 SQL queries to answer specific business questions. The full script can be found in `customer_behavior_sql_queries.sql`.

5.  **Visualization:**
    * [cite_start]Connected Power BI to the PostgreSQL database to build an interactive dashboard summarizing the key metrics and findings[cite: 62, 63].

---

## 💡 Key Insights & Findings

The SQL analysis revealed several key insights:

* [cite_start]**Revenue by Gender:** Male customers generated more than double the revenue ($157,890) compared to female customers ($75,191)[cite: 34, 37, 141, 142].
* [cite_start]**Subscription Status:** Non-subscribers make up the vast majority of the customer base (73%) and generate significantly more total revenue ($170,436) than subscribers ($62,645)[cite: 49, 80, 90, 177, 181]. [cite_start]The average spend between the two groups is nearly identical[cite: 49, 176, 180].
* [cite_start]**Customer Segmentation:** The customer base is heavily skewed towards "Loyal" customers (3,116), followed by "Returning" (701) and "New" (83)[cite: 54, 166, 169, 172].
* [cite_start]**Shipping & Spending:** Customers using `Express` shipping have a slightly higher average purchase amount ($60.48) than those using `Standard` shipping ($58.46)[cite: 46, 144, 145].
* [cite_start]**Discount-Dependent Products:** `Hat` and `Sneakers` are the most discount-dependent, with approximately 50% of their sales involving a discount[cite: 52, 159, 160].
* **Top Products by Category:**
    * [cite_start]**Accessories:** Jewelry (171 orders) [cite: 57, 185]
    * [cite_start]**Clothing:** Blouse (171 orders) [cite: 57, 186]
    * [cite_start]**Footwear:** Sandals (160 orders) [cite: 57, 187]
    * [cite_start]**Outerwear:** Jacket (163 orders) [cite: 57, 188]

---

## 📈 Business Recommendations

Based on the analysis, the following strategic recommendations are proposed:

1.  **Boost Subscriptions:**
    [cite_start]Develop a campaign to convert the large, high-revenue "Non-Subscriber" base by promoting exclusive benefits, as their current spending habits are already strong[cite: 99, 190].

2.  **Enhance Loyalty Programs:**
    [cite_start]Create targeted loyalty programs to reward the 701 "Returning" customers and incentivize them to move into the "Loyal" segment[cite: 102, 192].

3.  **Implement Targeted Marketing:**
    [cite_start]Focus marketing efforts on high-revenue demographic groups, such as "Young Adults" (who generated $62,143 in revenue) and customers who prefer Express shipping[cite: 61, 105, 147, 195].

4.  **Optimize Product Positioning:**
    [cite_start]Highlight top-rated products (e.g., Gloves, Sandals) and best-selling items (e.g., Jewelry, Blouse) in marketing campaigns to leverage their existing popularity[cite: 104, 197].

---

## 📁 Repository Structure

* `/Customer Shopping Behavior Analysis.pdf`: Final project report.
* `/Customer-Shopping-Behavior-Analysis.pptx`: Summary presentation slides.
* `/customer_behavior_sql_queries.sql`: All 10 SQL queries used for the analysis.
* `/images/dashboard.png`: Screenshot of the final Power BI dashboard.
* `README.md`: This file.
