# Customer Shopping Behavior Analysis

An end-to-end data analytics project focused on analyzing customer shopping behavior using transactional retail data. This project leverages Python, PostgreSQL, and Power BI to uncover insights related to customer spending patterns, product preferences, subscriptions, discounts, and customer segmentation. :contentReference[oaicite:0]{index=0}

---

## Project Overview

This project analyzes customer shopping behavior using transactional data from 3,900 purchases across multiple product categories. The primary objective is to identify meaningful business insights that can help improve customer retention, increase revenue, optimize discounts, and support data-driven marketing strategies. :contentReference[oaicite:1]{index=1}

The project workflow includes:
- Data Cleaning & Preprocessing using Python
- Exploratory Data Analysis (EDA)
- SQL-based Business Analysis using PostgreSQL
- Interactive Dashboard Development in Power BI
- Business Recommendation Generation

---

## Dataset Summary

The dataset contains customer demographics, purchase information, and shopping behavior data. :contentReference[oaicite:2]{index=2}

### Dataset Details
- Rows: 3,900
- Columns: 18

### Key Features
- Customer demographics (Age, Gender, Location, Subscription Status)
- Purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color)
- Shopping behavior (Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type)

### Data Quality
- 37 missing values in the Review Rating column

---

## Tools & Technologies Used

- Python
- Pandas
- PostgreSQL
- SQL
- Power BI
- Data Visualization
- Business Analytics

---

## Data Cleaning & Preprocessing

The initial data preparation was performed using Python. :contentReference[oaicite:3]{index=3}

### Tasks Performed
- Loaded dataset using pandas
- Performed exploratory analysis using `df.info()` and `describe()`
- Handled missing values in Review Rating using median imputation
- Standardized column names into snake_case
- Created new features for better analysis
- Removed redundant columns
- Loaded cleaned data into PostgreSQL for SQL analysis

### Feature Engineering
- Created `age_group` column
- Created `purchase_frequency_days` column

---

## SQL Business Analysis

Business-focused analysis was performed using PostgreSQL queries. :contentReference[oaicite:4]{index=4}

### Key SQL Analyses

1. Revenue by Gender
2. High-Spending Discount Users
3. Top 5 Products by Rating
4. Shipping Type Comparison
5. Subscribers vs Non-Subscribers Analysis
6. Discount-Dependent Products
7. Customer Segmentation
8. Top 3 Products per Category
9. Repeat Buyers & Subscription Analysis
10. Revenue by Age Group

---

## Example SQL Queries

### Revenue by Gender

```sql
SELECT gender, SUM(purchase_amount) AS revenue
FROM customer_shopping
GROUP BY gender;
```

### Top 5 Products by Rating

```sql
SELECT item_purchased,
AVG(review_rating) AS average_product_rating
FROM customer_shopping
GROUP BY item_purchased
ORDER BY average_product_rating DESC
LIMIT 5;
```

### Customer Segmentation

```sql
SELECT customer_segment,
COUNT(*) AS number_of_customers
FROM customer_segments
GROUP BY customer_segment;
```

---

## Power BI Dashboard

An interactive Power BI dashboard was created to visualize customer shopping insights. :contentReference[oaicite:5]{index=5}

### Dashboard Features
- Total Customers KPI
- Average Purchase Amount
- Average Review Rating
- Revenue by Category
- Sales by Category
- Revenue by Age Group
- Subscription Analysis
- Sales by Age Group

### Interactive Filters
- Gender
- Subscription Status
- Category
- Shipping Type

---

## Key Insights

### Revenue Insights
- Male customers generated higher total revenue compared to female customers. :contentReference[oaicite:6]{index=6}

### Customer Segmentation
- Loyal customers formed the largest customer segment. :contentReference[oaicite:7]{index=7}

### Product Insights
- Gloves, Sandals, and Boots received the highest average ratings. :contentReference[oaicite:8]{index=8}

### Discount Analysis
- Certain products heavily depended on discounts to drive sales. :contentReference[oaicite:9]{index=9}

### Subscription Analysis
- Non-subscribers contributed more total revenue overall. :contentReference[oaicite:10]{index=10}

---

## Business Recommendations

Based on the analysis, the following recommendations were proposed: :contentReference[oaicite:11]{index=11}

- Boost subscription programs with exclusive customer benefits
- Introduce customer loyalty rewards for repeat buyers
- Optimize discount policies for better profit margins
- Promote top-rated and best-selling products
- Focus marketing campaigns on high-revenue customer groups

---

## Project Structure

```bash
Customer-Shopping-Behavior-Analysis/
│
├── Dataset/
│   └── customer_shopping_data.csv
│
├── Python/
│   └── data_cleaning_and_eda.ipynb
│
├── SQL/
│   └── business_analysis.sql
│
├── PowerBI/
│   └── customer_behavior_dashboard.pbix
│
├── Images/
│   └── dashboard_screenshots
│
└── README.md
```

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- SQL Query Writing
- PostgreSQL Database Handling
- Power BI Dashboard Development
- Data Visualization
- Business Analytics
- Customer Segmentation
- Feature Engineering

---

## Learning Outcomes

Through this project, I gained practical experience in:

- End-to-end data analytics workflow
- Customer behavior analysis
- SQL-based business problem solving
- Dashboard creation in Power BI
- Data storytelling and insight generation
- Business recommendation development

---

## Future Improvements

- Add machine learning models for customer purchase prediction
- Build recommendation systems
- Integrate real-time sales dashboards
- Perform advanced customer segmentation
- Deploy dashboards online for live business monitoring

---

## Author

**Abhinav Mishra**  
B.Tech CSE | Data Analytics & Full Stack Development Enthusiast

- GitHub: Add your GitHub link
- LinkedIn: Add your LinkedIn link

---

## Project Reference

Customer Shopping Behavior Analysis Project using Python, PostgreSQL, SQL, and Power BI. :contentReference[oaicite:12]{index=12}
