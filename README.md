# 🛒 Zepto E-commerce SQL Data Analysis

A practical **SQL Data Analytics portfolio project** focused on analyzing e-commerce inventory data inspired by Zepto's quick-commerce product catalog.

This project demonstrates how SQL can be used to transform raw product and inventory data into meaningful business insights around **pricing, discounts, inventory, stock availability, product value, and category performance**.

The project follows a complete data analyst workflow:

**Raw Data → Data Exploration → Data Cleaning → SQL Analysis → Business Insights**

---

## 📌 Project Overview

E-commerce businesses manage thousands of products with different prices, discounts, package sizes, inventory levels, and stock statuses.

In this project, I use SQL to analyze an e-commerce inventory dataset and answer business-oriented questions such as:

- Which products have the highest discounts?
- Which expensive products are out of stock?
- Which categories have the highest potential inventory value?
- Which products provide better value based on price per gram?
- Which categories offer the highest average discounts?
- How is inventory distributed across different categories?
- How are products distributed based on their weight?

The project is designed to demonstrate practical SQL skills that can be applied to **retail, e-commerce, inventory, and product analytics**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Explore an e-commerce inventory dataset
- Create and manage a PostgreSQL table
- Identify missing and inconsistent data
- Clean invalid pricing records
- Convert prices from paise to Indian Rupees
- Analyze product availability
- Analyze discounts and pricing
- Estimate potential inventory value
- Compare products using price-per-gram analysis
- Analyze inventory across product categories
- Practice real-world SQL data analysis

---

## 📂 Dataset

The dataset used in this project is the **Zepto Inventory Dataset**, available on Kaggle.

### Dataset Source

**Kaggle:**  
https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset

The dataset contains product-level information including:

- Product name
- Category
- MRP
- Discount percentage
- Discounted selling price
- Available quantity
- Product weight
- Stock availability
- Package quantity

> **Note:** The dataset contains multiple SKUs, so the same product name may appear more than once due to different package sizes, quantities, or product variations.

---

## 🧾 Dataset Columns

| Column | Description |
|---|---|
| `sku_id` | Unique identifier for each SKU |
| `category` | Product category |
| `name` | Product name |
| `mrp` | Maximum Retail Price |
| `discountPercent` | Discount percentage |
| `discountedSellingPrice` | Final selling price after discount |
| `availableQuantity` | Quantity currently available |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Indicates whether the product is out of stock |
| `quantity` | Number of units in the package |

---

## 🛠️ Tools & Technologies

- PostgreSQL
- pgAdmin
- SQL
- CSV
- Git
- GitHub

---

## 🗃️ Database Schema

The dataset is stored in a PostgreSQL table named `zepto`.

```sql
CREATE TABLE zepto (
    sku_id SERIAL PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INTEGER,
    discountedSellingPrice NUMERIC(8,2),
    weightInGms INTEGER,
    outOfStock BOOLEAN,
    quantity INTEGER
);
