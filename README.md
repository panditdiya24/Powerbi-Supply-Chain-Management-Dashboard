# Powerbi-Supply-Chain-Management-Dashboard

## Overview
This project presents an interactive Power BI dashboard designed to analyze supply chain performance, inventory levels, sales revenue, and delivery fulfillments across various store locations.

## Key Metrics & Features
* **Total Sales Revenue & Orders:** Detailed order volume tracking by purchase method and customer region.
* **Inventory Analysis:** Stock-on-hand tracking using adjusted inventory data (`f_inventory_adjusted`).
* **Store Performance:** Breakdown of spatial metrics, rent costs, and revenue across physical store locations.
* **Calendar Integration:** Time-series performance broken down by fiscal years, quarters, and seasons.
  
## Dashboard Preview
<img width="1422" height="797" alt="image" src="https://github.com/user-attachments/assets/d839572e-2f36-436a-bcd1-f672f6849e00" />

## Data Sources & Schema
* `f_sales`: Transaction and order details.
* `f_inventory_adjusted`: Product stock, pricing, and cost analysis.
* `d_store`: Store location, size, and operational data.
* `customer`: Demographic and purchasing behavior.

## Tools & Concepts Used
* Power BI Desktop
* DAX Measures (CALCULATE, SUMMARIZE)
* Data Modeling (Star Schema)
