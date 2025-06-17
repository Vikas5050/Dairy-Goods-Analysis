# 🐄 Dairy Farm Power BI Analytics Dashboard
![Image](https://github.com/user-attachments/assets/fdb8aa12-b3e2-451b-9414-2d3ae8b997a6)
This project presents a comprehensive **Power BI dashboard** designed to analyze various aspects of a dairy farm's operations, including performance by location and farm size, product sales trends, shelf life and storage impacts, and revenue generation across customer regions and brands.

---

## 📁 Dataset Description

The dataset consists of structured information related to:

### 🐄 Farm Attributes
- **Location**: Geographic area of the farm
- **Total Land Area (acres)**: Size of land owned
- **Number of Cows**: Cow population on each farm
- **Farm Size (sq.km)**: Physical area covered by the farm
- **Date**: Data recording date

### 🧀 Product Information
- **Product ID / Name / Brand**
- **Quantity (liters/kg)**
- **Price per Unit**
- **Shelf Life (days)**
- **Storage Condition**
- **Production Date**
- **Expiration Date**

### 💰 Sales & Inventory
- **Quantity Sold (liters/kg)**
- **Price per Unit (Sold)**
- **Approx. Total Revenue (INR)**
- **Customer Location**
- **Sales Channel (Retail, Wholesale, Online)**
- **Quantity in Stock**
- **Minimum Stock Threshold**
- **Reorder Quantity**

---

## 🎯 Project Objectives

### 1️⃣ Dairy Farm Performance Analysis
- Evaluate performance based on **farm size**, **location**, and **cow population**
- Compare land utilization and livestock density across regions

### 2️⃣ Sales & Distribution Patterns
- Understand **revenue trends** by **brand** and **location**
- Visualize **quantity sold** across product-brand combinations
- Analyze **sales channel performance** in different regions

### 3️⃣ Product Shelf Life & Storage Condition
- Study how **storage conditions** affect **average shelf life**
- Compare **minimum and maximum shelf life** of products
- Identify products with shorter or longer expiration durations

### 4️⃣ Inventory Insights
- Track quantity in stock vs minimum threshold
- Provide stock levels by product and brand
- Plan future inventory actions (e.g., restocking) based on demand and threshold data

---

## 📊 Visuals & Insights

The dashboard includes:

- 💰 **Total Revenue Card with Brand Slicer**
- 🐄 **Multi-row Card:** Total Land Area and Number of Cows
- 📊 **Clustered Column-Line Chart:** Farm Location vs. Total Land Area & Cow Count
- 📊 **Clustered Column Chart:** Revenue by Location with Farm Size Slicer
- 📈 **Sales Volume by Brand and Product Name**
- 🌍 **Revenue by Customer Location and Sales Channel**
- 📦 **Shelf Life (Min/Max) by Product Name**
- ❄️ **Average Shelf Life by Storage Condition**
- ⏳ **Average Expiry Duration by Product Name**

---

## 🧠 DAX Calculations

### ✅ Custom Column: Expiry Duration (in days)
```DAX
Expiry Duration = 'dairy_dataset'[Expiration Date] - 'dairy_dataset'[Date]
