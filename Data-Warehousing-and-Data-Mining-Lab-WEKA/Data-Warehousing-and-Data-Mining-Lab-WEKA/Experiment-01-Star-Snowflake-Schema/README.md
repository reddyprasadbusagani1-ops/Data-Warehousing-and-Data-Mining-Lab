# Experiment 1: Create Star and Snowflake Schemas Using SQL

## Aim
To design Star and Snowflake schemas for a sample sales data warehouse using SQL.

## Theory
A Star schema stores descriptive attributes in denormalized dimension tables connected to a central fact table. A Snowflake schema normalizes dimension data into related sub-dimension tables.

## SQL — Star schema
```sql
CREATE TABLE dim_date (
    date_key INT PRIMARY KEY,
    full_date DATE,
    month_name VARCHAR(20),
    quarter_no INT,
    year_no INT
);

CREATE TABLE dim_product (
    product_key INT PRIMARY KEY,
    product_name VARCHAR(100),
    category VARCHAR(50)
);

CREATE TABLE dim_store (
    store_key INT PRIMARY KEY,
    store_name VARCHAR(100),
    city VARCHAR(60),
    state_name VARCHAR(60)
);

CREATE TABLE fact_sales (
    sales_key INT PRIMARY KEY,
    date_key INT,
    product_key INT,
    store_key INT,
    quantity INT,
    sales_amount DECIMAL(12,2),
    FOREIGN KEY (date_key) REFERENCES dim_date(date_key),
    FOREIGN KEY (product_key) REFERENCES dim_product(product_key),
    FOREIGN KEY (store_key) REFERENCES dim_store(store_key)
);
```

## SQL — Snowflake schema variant
Use normalized product and location dimensions:
```sql
CREATE TABLE dim_category (
    category_key INT PRIMARY KEY,
    category_name VARCHAR(50)
);

CREATE TABLE dim_product_snow (
    product_key INT PRIMARY KEY,
    product_name VARCHAR(100),
    category_key INT,
    FOREIGN KEY (category_key) REFERENCES dim_category(category_key)
);

CREATE TABLE dim_state (
    state_key INT PRIMARY KEY,
    state_name VARCHAR(60)
);

CREATE TABLE dim_city (
    city_key INT PRIMARY KEY,
    city_name VARCHAR(60),
    state_key INT,
    FOREIGN KEY (state_key) REFERENCES dim_state(state_key)
);

CREATE TABLE dim_store_snow (
    store_key INT PRIMARY KEY,
    store_name VARCHAR(100),
    city_key INT,
    FOREIGN KEY (city_key) REFERENCES dim_city(city_key)
);
```
The fact table can reference `dim_product_snow` and `dim_store_snow` in a snowflake implementation.

## Procedure
1. Open your SQL client and connect to a test database.
2. Execute the Star schema statements.
3. Inspect tables and foreign-key relationships.
4. Execute the Snowflake dimension statements in a separate schema/database or with distinct table names.
5. Draw and include both schema diagrams in your record.

## Result
The SQL statements define sample Star and Snowflake warehouse structures. Execute them in your selected DBMS and attach the verified schema diagram/output.
