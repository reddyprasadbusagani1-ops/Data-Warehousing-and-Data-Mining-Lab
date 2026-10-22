# Experiment 2: OLAP Operations Using SQL

## Aim
To perform roll-up, drill-down, slice, dice, and pivot-style analysis on sales data.

## Sample query setup
Assume Experiment 1 tables exist and contain sample rows in `dim_date`, `dim_product`, `dim_store`, and `fact_sales`.

## Roll-up: aggregate sales by year
```sql
SELECT d.year_no, SUM(f.sales_amount) AS total_sales
FROM fact_sales f
JOIN dim_date d ON f.date_key = d.date_key
GROUP BY d.year_no
ORDER BY d.year_no;
```

## Drill-down: year to month
```sql
SELECT d.year_no, d.month_name, SUM(f.sales_amount) AS total_sales
FROM fact_sales f
JOIN dim_date d ON f.date_key = d.date_key
GROUP BY d.year_no, d.month_name
ORDER BY d.year_no, d.month_name;
```

## Slice: one year
```sql
SELECT d.year_no, p.category, SUM(f.sales_amount) AS total_sales
FROM fact_sales f
JOIN dim_date d ON f.date_key = d.date_key
JOIN dim_product p ON f.product_key = p.product_key
WHERE d.year_no = 2025
GROUP BY d.year_no, p.category;
```

## Dice: selected years and categories
```sql
SELECT d.year_no, p.category, s.city, SUM(f.sales_amount) AS total_sales
FROM fact_sales f
JOIN dim_date d ON f.date_key = d.date_key
JOIN dim_product p ON f.product_key = p.product_key
JOIN dim_store s ON f.store_key = s.store_key
WHERE d.year_no IN (2024, 2025)
  AND p.category IN ('Electronics', 'Stationery')
  AND s.city IN ('Punganur', 'Tirupati')
GROUP BY d.year_no, p.category, s.city;
```

## Pivot-style report
Conditional aggregation is broadly portable compared with vendor-specific `PIVOT` syntax:
```sql
SELECT p.category,
       SUM(CASE WHEN d.year_no = 2024 THEN f.sales_amount ELSE 0 END) AS sales_2024,
       SUM(CASE WHEN d.year_no = 2025 THEN f.sales_amount ELSE 0 END) AS sales_2025
FROM fact_sales f
JOIN dim_date d ON f.date_key = d.date_key
JOIN dim_product p ON f.product_key = p.product_key
GROUP BY p.category;
```

## Procedure
1. Run the queries after inserting data into the warehouse tables.
2. Compare the level of detail in roll-up and drill-down.
3. Record the filter conditions used for slice and dice.
4. Capture query results from your DBMS.

## Result
The SQL examples demonstrate common OLAP analysis patterns. Actual result rows depend on the data inserted into the tables.
