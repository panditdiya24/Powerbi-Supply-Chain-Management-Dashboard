# Powerbi-Supply-Chain-Management-Dashboard

## Overview
An interactive Power BI dashboard analyzing end-to-end supply chain performance, sales revenue, inventory health, order delivery SLAs, and supplier reliability.

## Key Metrics & Analytics
* **Sales & Revenue Performance:** Tracks order volume, total revenue, COGS, and shipping costs derived from order fulfillments (`Fact_Orders`).
* **Inventory & Stock Health:** Monitors monthly stock-on-hand, safety stock levels, reorder triggers, days of supply, and stockout occurrences (`Fact_Inventory`).
* **Logistics & Delivery SLA:** Analyzes lead times, processing/transit days, fill rate percentage (`Fill_Rate_Pct`), and delivery timeliness (`Delivery_Status`).
* **Supplier & Warehouse Analytics:** Evaluates supplier reliability scores (`Reliability_Score`), supplier tiers (A/B/C), and regional warehouse capacities (`Capacity_Units`).

## Data Sources & Schema
This project uses **`Supply_Chain_Dataset.xlsx`**, structured as a Star Schema with two fact tables and four dimension tables:

| Table Name | Schema Type | Primary Key | Key Columns & Description |
| :--- | :--- | :--- | :--- |
| **`Fact_Orders`** | Fact Table | `Order_ID` | Order line transactions including `Order_Date`, `Actual_Delivery_Date`, `Revenue`, `COGS`, `Shipping_Cost`, `Delivery_Status`, and `Fill_Rate_Pct`. |
| **`Fact_Inventory`** | Fact Table | (`Product_ID`, `Warehouse_ID`, `Snapshot_Date`) | Monthly inventory snapshots tracking `Stock_On_Hand`, `Reorder_Level`, `Safety_Stock`, `Days_Of_Supply`, and `Stockout_Flag`. |
| **`Dim_Product`** | Dimension | `Product_ID` | Product details including `Product_Name`, `Category`, `Sub_Category`, `Unit_Cost`, `Unit_Price`, and `Primary_Supplier_ID`. |
| **`Dim_Supplier`** | Dimension | `Supplier_ID` | Vendor metadata including `Supplier_Name`, `Supplier_Country`, `Supplier_Tier`, and `Reliability_Score`. |
| **`Dim_Warehouse`** | Dimension | `Warehouse_ID` | Facility data including `Warehouse_City`, `Warehouse_Region`, and `Capacity_Units`. |
| **`Dim_Customer`** | Dimension | `Customer_ID` | Customer profile attributes including `Customer_Region`, `Customer_Country`, and `Customer_Segment` (Retail, Corporate, Wholesale, E-commerce). |
| **`Data_Dictionary`** | Reference | N/A | Complete dictionary specifying column definitions, data types, and grain relationships. |
  
## Dashboard Preview
<img width="1422" height="797" alt="image" src="https://github.com/user-attachments/assets/d839572e-2f36-436a-bcd1-f672f6849e00" />

## Tools & Concepts Used
* Power BI Desktop
* DAX Measures (CALCULATE, SUMMARIZE)
* Data Modeling (Star Schema)
