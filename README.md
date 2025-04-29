
---

## 🎯 Objectives

- Track order performance and monthly sales trends  
- Identify top customers and new vs. returning behavior  
- Analyze payment success/failure patterns  
- Deliver clean, report-ready output for BI tools

---

## 🧰 Tools & Technologies

- **SQL (PostgreSQL / MySQL compatible)**
- **Power BI** (for dashboard/report visualization)
- Optional: Python/Excel for ETL or exploration

---

## 📊 Dataset Overview

### `customer_orders.csv`
| Column         | Description                 |
|----------------|-----------------------------|
| order_id       | Unique order identifier     |
| customer_id    | Unique customer identifier  |
| order_date     | Date of order placed        |
| order_status   | Order status (placed, canceled, etc.) |
| order_amount   | Total value of the order    |

### `payments.csv`
| Column         | Description                   |
|----------------|-------------------------------|
| payment_id     | Unique payment ID             |
| order_id       | Related order ID              |
| payment_date   | Date of payment               |
| payment_status | Payment status (success, failed, etc.) |
| payment_amount | Amount paid                   |
| payment_method | Method used (card, wallet, etc.) |

---

## 📌 SQL Modules

### 📁 1. Order & Sales Analysis
**Goal:** Measure performance by order status and time  
- `order_status` breakdown with total sales  
- Monthly revenue trends and growth rates  
- Average order value by status

📄 [`1_order_sales_analysis.sql`](queries/1_order_sales_analysis.sql)

---

### 📁 2. Customer Analysis
**Goal:** Understand acquisition and loyalty  
- Top customers by orders and revenue  
- Monthly new customers  
- Split between new vs. returning customers

📄 [`2_customer_analysis.sql`](queries/2_customer_analysis.sql)

---

### 📁 3. Payment Status Analysis  
**Goal:** Evaluate payment health and timing  
- Total payments by success/failure  
- Monthly payment failure rate  
- Average time between order and payment by status

📄 [`3_payment_status_analysis.sql`](queries/3_payment_status_analysis.sql)

---

### 📁 4. Order Details Report  
**Goal:** Build report-friendly output  
- One-row-per-order with payment summary  
- All payment attempts per order (for audit)

📄 [`4_order_details_report.sql`](queries/4_order_details_report.sql)

---

## 📈 Sample Insights (based on mock data)
- Most revenue comes from orders in `placed` status, with high AOV
- Revenue peaks in Q4, showing strong holiday performance
- Payment failure rate rose in March due to gateway issues
- 35% of monthly orders come from returning customers

---

## 📌 How to Run

1. Import `.csv` files into your SQL database (MySQL/PostgreSQL)
2. Run SQL scripts from the `queries/` folder sequentially
3. Optionally load outputs into Power BI for dashboards

---

## 📊 Optional: Power BI Dashboard

- Import cleaned queries into Power BI
- Create visualizations for:
  - Monthly sales growth
  - Payment success trends
  - Top customer leaderboard
  - New vs. returning order ratio

---

## 🧠 Future Enhancements

- Integrate customer segmentation (RFM analysis)
- Predict late payments using logistic regression
- Automate report refresh using Power BI service or Python scripts

---

## 👨‍💻 Author

**Abhishek Das**  
📍 Data Analyst | SQL | Python | Power BI  
📫 Email: theabhishekdas09@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/your-link) | [GitHub](https://github.com/your-profile)

---

> *Feel free to fork, star ⭐ and contribute to improve this analysis framework.*

