# 🛒 E-commerce Business Intelligence 360

## 📌 Project Overview

E-commerce Business Intelligence 360 is a data analytics and visualization project built using **MySQL and Microsoft Power BI**. It transforms e-commerce transactional data into interactive dashboards to help analyze sales performance, customer behavior, order fulfillment, product performance, and payment trends.

The project demonstrates an end-to-end analytics workflow, from querying relational data in MySQL to building business-focused KPIs and interactive reports in Power BI.

> **Note:** This portfolio project uses sample data for learning and demonstration purposes.

## 🎯 Business Objectives

- Monitor overall sales and order performance.
- Analyze revenue and gross profit.
- Track order fulfillment, cancellations, and returns.
- Understand customer and product performance.
- Analyze sales trends and business KPIs.
- Present actionable insights through interactive dashboards.

## 🛠️ Tools & Technologies

- **MySQL** — Database management and SQL analysis.
- **Microsoft Power BI** — Dashboard development and visualization.
- **DAX** — KPI calculations and business measures.
- **Power Query** — Data preparation and transformation.
- **Data Modeling** — Relationships between customers, products, orders, order items, and payments.

## 🗂️ Database Structure

The project uses the `ecommerce_bi360` database with these main tables:

| Table | Purpose |
|---|---|
| `customers` | Customer information |
| `products` | Product details, categories, prices, and costs |
| `orders` | Order dates, customers, order status, and sales channel |
| `order_items` | Products, quantities, discounts, and order-level item details |
| `payments` | Payment methods and payment statuses |

## 📊 Power BI Dashboard Pages

### 1. Executive Overview

Provides a high-level summary of business performance using KPI cards and visualizations.

Key metrics include:
- Total Sales
- Gross Profit
- Profit Margin %
- Average Order Value (AOV)
- Total Orders
- Total Customers
- Total Quantity Sold
- Delivered, Cancelled, and Returned Orders

![E-commerce BI 360 Executive Overview](Ecommerce_BI360_Dashboard%20Executive%20Overview.png)

### 2. Sales & Performance Analysis

Focuses on exploring sales performance and business trends through interactive visuals and filters.

The page supports analysis of sales trends, order performance, and business results across the available data dimensions.

![E-commerce BI 360 Sales & Performance Analysis](Ecommerce_BI360_Dashboard%20Sales%20and%20Performance%20Analysis.png)

## 🧮 Example DAX Measures

### Total Sales

```dax
Total Sales =
SUMX(
    order_items,
    order_items[quantity] *
    order_items[unit_cost]
)
```

**Important:** Verify that `unit_cost` represents the selling price before using this formula as Total Sales. If it is the product cost, replace it with the appropriate selling-price column, such as `list_price`, and account for discounts.

### Profit Margin %

```dax
Profit Margin % =
DIVIDE(
    [Gross Profit],
    [Total Sales],
    0
)
```

### Average Order Value

```dax
Average Order Value =
DIVIDE(
    [Total Sales],
    [Total Orders],
    0
)
```

## 🔍 Key Business Insights

The dashboard is designed to help users:

- Understand overall revenue and profitability.
- Monitor order fulfillment and identify cancelled or returned orders.
- Compare performance across products and customers.
- Explore changes in sales over time.
- Support data-driven business decisions.

## 📁 Repository Contents

| File | Description |
|---|---|
| `Ecommerce_BI360_Analysis.sql.pbix` | Power BI report file |
| `Ecommerce_BI360_Dashboard Executive Overview.png` | Executive Overview screenshot |
| `Ecommerce_BI360_Dashboard Sales and Performance Analysis.png` | Sales & Performance Analysis screenshot |
| `README.md` | Project documentation |

## 🚀 Skills Demonstrated

- SQL and relational database analysis
- Data cleaning and transformation
- Data modeling
- DAX measures and KPI development
- Interactive dashboard design
- Business performance analysis
- Data storytelling and visualization

## 👨‍💻 Project Purpose

This project is part of my data analytics portfolio, demonstrating how SQL and Power BI can be combined to transform transactional data into meaningful business insights.
I am continuing to develop my skills in data analytics, business intelligence, and Power BI development.

👤 Author

**Manohar Kuttuboina**
Aspiring Power BI Developer | Data Analytics Portfolio

This project was developed for learning and portfolio demonstration using synthetic sample data.
