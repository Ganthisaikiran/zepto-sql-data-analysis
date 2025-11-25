🛒 Zepto SQL Data Analysis Project

A simple and clean SQL portfolio project I tried based on Zepto’s e-commerce inventory data.

This project helped me understand how real e-commerce companies manage their product stock, pricing, and discounts — and how data analysts use SQL in actual business situations.

📌 What This Project Is About

Using PostgreSQL and a real-looking dataset from Zepto, I did:

Setting up an e-commerce-style database

Exploring messy raw data

Cleaning data (fixing errors, removing bad rows, converting prices)

Writing SQL queries to find business insights like stock availability, revenue, discounts, etc.

This is a perfect beginner-friendly SQL project to add to a portfolio.

📁 Dataset Info 

Each row in the dataset is one SKU basically one product entry on Zepto.

Here are the columns in easy words:

sku_id – unique ID (auto-generated)

name – product name

category – type of product (Snacks, Fruits, Beverages, etc.)

mrp – original price

discountPercent – discount

discountedSellingPrice – final selling price

availableQuantity – how much stock is available

weightInGms – product weight

outOfStock – true/false

quantity – number of units per packet

The dataset was scraped from Zepto, so it feels like real e-commerce data—messy, repeated items, different weights, different prices, etc.

🔧 Project Workflow (What I Did Step-By-Step)
1️⃣ Created a Table
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

2️⃣ Imported the CSV

Tried pgAdmin import

Fixed UTF-8 errors by resaving the CSV

Used \copy command when import didn’t work

3️⃣ Explored the Data

I checked:

Total row count

Sample rows

Null values

Unique categories

Out-of-stock vs in-stock items

Duplicate product names (different SKUs)

4️⃣ Cleaned the Data

Removed rows where price was 0

Converted paise → rupees

Checked price consistency

5️⃣ Business Insights (Main Analysis)

I wrote SQL queries to find:

Top 10 highest discounts

Expensive products that are out of stock

Revenue potential by category

Categories with highest average discounts

Price per gram values

Inventory weight distribution

Grouping products into low/medium/bulk weight groups

These are common tasks in e-commerce analytics.


