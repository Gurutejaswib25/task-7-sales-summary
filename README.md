# Task 7: Basic Sales Summary Using Python and SQLite

## 📌 Objective
The goal of this task is to use Python to connect to a SQLite database, perform SQL queries to summarize sales data, and visualize the results using a simple bar chart.

---

## 🧰 Tools Used
- **Google Colab** (Python 3)
- **SQLite** (via `sqlite3` library)
- **Pandas** (for handling query results)
- **Matplotlib** (for plotting revenue by product)

---

## 🗃️ Dataset
The SQLite database is named `sales_data.db`, containing a single table: `sales`.

### Table: `sales`

| Column   | Type    | Description         |
|----------|---------|---------------------|
| `id`     | INTEGER | Unique row ID       |
| `product`| TEXT    | Product name        |
| `quantity` | INTEGER | Number of items sold |
| `price`  | REAL    | Price per item      |

Sample data was inserted using Python and consists of multiple sales entries for products like Apples, Bananas, Oranges, and Grapes.

---

## 🧠 SQL Query Used

```sql
SELECT 
  product,
  SUM(quantity) AS total_qty,
  SUM(quantity * price) AS revenue
FROM sales
GROUP BY product
Done By:
BOMMIDI GURU TEJASWI
