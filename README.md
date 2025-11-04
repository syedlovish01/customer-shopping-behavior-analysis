# 👨🏻‍💻Customer Behavior Data Analyst Portfolio Project

This project performs an end-to-end analysis of customer shopping behavior based on 3,900 transactional records[cite: 3]. [cite_start]The goal is to uncover actionable insights into spending patterns, customer segments, product preferences, and subscription behavior to inform strategic business decisions.


---

## 🛠️ Technology Stack

This analysis was conducted using the following tools:

* **Python (Pandas):** For data loading, cleaning, preprocessing, and feature engineering.
* **PostgreSQL (SQL):** For in-depth data analysis and answering key business questions by querying the cleaned data.
* **Power BI:** For creating a final interactive dashboard to visualize the findings.

---

## ⚙️ Project Workflow

The project followed a structured data analysis process:

1.  **Data Cleaning (Python):**
    * Loaded the dataset (3,900 rows, 18 columns) into a pandas DataFrame.
    * Handled 37 missing `Review Rating` values by imputing the median rating for each product's category.
    * Standardized column names to `snake_case` for better readability and SQL compatibility.

2.  **Feature Engineering (Python):**
    * Created a new `age_group` column by binning customer ages.
    * Checked for data redundancy and dropped the `promo_code_used` column, as `discount_applied` captured the necessary information.

3.  **Database Integration:**
    * Loaded the cleaned and transformed DataFrame into a PostgreSQL database for structured querying.

4.  **SQL Analysis:**
    * Wrote 10 SQL queries to answer specific business questions. The full script can be found in `customer_behavior_sql_queries.sql`.

5.  **Visualization:**
    * Connected Power BI to the PostgreSQL database to build an interactive dashboard summarizing the key metrics and findings.

---

## 💡 Key Insights & Findings

The SQL analysis revealed several key insights:

* **Revenue by Gender:** Male customers generated more than double the revenue ($157,890) compared to female customers ($75,191).
* **Subscription Status:** Non-subscribers make up the vast majority of the customer base (73%) and generate significantly more total revenue ($170,436) than subscribers ($62,645). The average spend between the two groups is nearly identical.
* **Customer Segmentation:** The customer base is heavily skewed towards "Loyal" customers (3,116), followed by "Returning" (701) and "New" (83).
* **Shipping & Spending:** Customers using `Express` shipping have a slightly higher average purchase amount ($60.48) than those using `Standard` shipping ($58.46).
* **Discount-Dependent Products:** `Hat` and `Sneakers` are the most discount-dependent, with approximately 50% of their sales involving a discount.
* **Top Products by Category:**
    * **Accessories:** Jewelry (171 orders)
    * **Clothing:** Blouse (171 orders)
    * **Footwear:** Sandals (160 orders)
    * **Outerwear:** Jacket (163 orders)

---

## 📈 Business Recommendations

Based on the analysis, the following strategic recommendations are proposed:

1.  **Boost Subscriptions:**
    Develop a campaign to convert the large, high-revenue "Non-Subscriber" base by promoting exclusive benefits, as their current spending habits are already strong.

2.  **Enhance Loyalty Programs:**
    Create targeted loyalty programs to reward the 701 "Returning" customers and incentivize them to move into the "Loyal" segment.

3.  **Implement Targeted Marketing:**
    Focus marketing efforts on high-revenue demographic groups, such as "Young Adults" (who generated $62,143 in revenue) and customers who prefer Express shipping.

4.  **Optimize Product Positioning:**
    Highlight top-rated products (e.g., Gloves, Sandals) and best-selling items (e.g., Jewelry, Blouse) in marketing campaigns to leverage their existing popularity.

---

## 📁 Repository Structure

* `/Customer Shopping Behavior Analysis.pdf`: Final project report.
* `/Customer-Shopping-Behavior-Analysis.pptx`: Summary presentation slides.
* `/customer_behavior_sql_queries.sql`: All 10 SQL queries used for the analysis.
##                                               Screenshot of the final Power BI dashboard.
  ![image alt](https://github.com/syedlovish01/customer-shopping-behavior-analysis/blob/020d7c5e7742a743c73e67d99e3fbb70c579867a/customer_dashboard.jpeg): 
* `README.md`: This file.
