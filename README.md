# TASK6-DA-INTERN
# 📊 Task 6 - SQL-Based Data Analysis (Internship Project)

This project demonstrates how to perform **SQL-based exploratory data analysis (EDA)** inside **Google Colab** using an `orders` dataset. The analysis is powered by **SQLite3** and **Pandas**, working entirely in-memory — no database server required!

---

## 📁 Files

- `task6(DA intern).ipynb` – Jupyter Notebook containing SQL EDA steps
- `orders.csv` – Input dataset with order and product category columns

---

## 🔧 Technologies Used

- Python 3
- SQLite (via `sqlite3`)
- Pandas
- Google Colab

---

## 🚀 Features & Steps

1. **Upload Dataset** using Google Colab file upload
2. **Create SQLite DB** in memory and load the dataset into it
3. **Run SQL Queries** to analyze the data:
   - Total number of orders
   - Average order hour
   - Orders by day of the week
   - Top 5 most ordered product categories
4. **Visualize Product Popularity** (optional with Pandas + Seaborn)

---

## 📦 Columns in Dataset

- `order_id`, `order_dow`, `order_hour_of_day`, `days_since_prior_order`
- 130+ product category columns like:
  - `tea`, `yogurt`, `tofu meat alternatives`, `white wines`, etc.

---

## 📈 Sample SQL Queries Used

```sql
SELECT COUNT(*) FROM data_table;

SELECT AVG(order_hour_of_day) FROM data_table;

SELECT order_dow, COUNT(*) 
FROM data_table 
GROUP BY order_dow 
ORDER BY order_dow;
