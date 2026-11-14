<p align="center">
  
  <img width="488" height="383" alt="Roder_Shop_simple_Logo" src="https://github.com/user-attachments/assets/2182a9f2-cdbc-4e10-ad51-d1cd39699737" />
</p>

<h1 align="center">Roder Shop – Sales Tracking Dashboard (Power BI)</h1>

<p align="center">
  An interactive 4-page Power BI dashboard analysing sales, customers, products and orders of an office-supplies retailer (Superstore dataset, 2014–2017).
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/DAX-Measures-0F6CBD" alt="DAX">
  <img src="https://img.shields.io/badge/Data-Superstore%20(9,994%20rows)-1f4e8c" alt="Dataset">
  </p>

---

## 1. Business context

**Roder Shop** is a fictional office-supplies retailer selling Furniture, Office Supplies and Technology products to Consumer, Corporate and Home Office customers across four US regions.

The management team needs a single place to answer questions such as:

- How are **sales and profit** evolving over time, and where is the business most profitable?
- Who are the **most valuable customers**, and where are they located?
- Which **products and sub-categories** drive revenue, and which ones destroy margin?
- How do **shipping modes, segments and regions** split the order volume?

## 2. Dataset

| Item | Detail |
|---|---|
| Source | Sample – Superstore (Tableau sample dataset) |
| File | [`Sample_Superstore.csv`](Sample_Superstore.csv) |
| Grain | 1 row = 1 order line |
| Size | 9,994 rows × 21 columns |
| Period | 3 Jan 2014 → 30 Dec 2017 |
| Scope | 793 customers · 5,009 orders · 4 regions · United States |

**Full column descriptions:** 

| Column | Type | Description |
|---|---|---|
| Row ID | Integer | Unique row identifier |
| Order ID | Text | Order identifier (an order can have several lines) |
| Order Date | Date | Date the order was placed |
| Ship Date | Date | Date the order was shipped |
| Ship Mode | Text | Standard Class, Second Class, First Class, Same Day |
| Customer ID | Text | Unique customer identifier |
| Customer Name | Text | Customer full name |
| Segment | Text | Consumer, Corporate, Home Office |
| Country | Text | Country (United States) |
| City | Text | Delivery city |
| State | Text | Delivery state |
| Postal Code | Integer | Delivery postal code |
| Region | Text | West, East, Central, South |
| Product ID | Text | Product identifier |
| Category | Text | Furniture, Office Supplies, Technology |
| Sub-Category | Text | 17 sub-categories (Binders, Paper, Phones, Tables…) |
| Product Name | Text | Product name |
| Sales | Decimal | Revenue of the line ($) |
| Quantity | Integer | Units sold |
| Discount | Decimal | Discount applied (0–0.8) |
| Profit | Decimal | Profit of the line ($), can be negative |

## 3. Dashboard pages

### Page 1 – Overview of Sales Tracking

<img width="1369" height="747" alt="OverView_of_Sales" src="https://github.com/user-attachments/assets/999d3501-a18d-41a4-8d6b-c7ca976f052c" />

**•	Purpose:** Provides a high-level executive summary of overall business performance and core KPIs. 

**•	Key Metrics Tracked:** Total Sales ($2.30M), Total Profit ($286.4K), Total Orders (9,994), Total Customers (793), and overall Profit Margin (12.47%). 

**•	Visual Breakdown:**
**-	Top Performers:** Identifies the top 10 revenue-generating customers **(led by Sean Miller)** and top 10 products by sales and profit **(led by the Canon imageCLASS 2200 Advanced Copier)**. 

**-	Logistics & Geography:** Breaks down profit distribution by delivery mode **(Standard Class drives 57.29% of total profit)** and maps out the top 10 best-selling states across the U.S. **(with California and New York leading)**. 

**-	Time-Series Trends:** Tracks monthly sales and profit trajectories against a moving/average sales benchmark, highlighting strong Q4 revenue spikes. 


### Page 2 – Customer Analysis

<img width="1369" height="744" alt="Customers_Analysis" src="https://github.com/user-attachments/assets/e620b68f-0b9d-4797-a0ee-dc1350728738" />


**•	Purpose:** Analyzes customer demographics, purchasing behaviors, geographic concentration, and individual account profitability. 

**•	Key Insights & Visuals:**

**-	Segmentation & Preferences:** Breaks down the customer base by market segment **(Consumer: 51.58%, Corporate: 29.76%, Home Office: 18.66%)**, preferred product categories, and shipping methods. 

**-	Geographic Concentration:** Ranks top cities by customer volume, highlighting major hubs like **New York City (355), Los Angeles (304), and Philadelphia (239)**. 

**-	Account-Level Performance Table:** A detailed matrix evaluating individual customers across order frequency, unit quantity, total sales, net profit, and profit margin percentage **(e.g., Tamara Chand generating $19,052.22 in sales at a 47.14% margin)**. 


### Page 3 – Product Analysis

<img width="1369" height="743" alt="Products_Analysis" src="https://github.com/user-attachments/assets/5432cbb6-ad59-494b-b9f5-e4cae32cb579" />


**•	Purpose:** Evaluates catalog performance across categories, subcategories, and individual SKUs to pinpoint volume drivers versus margin drains. 

**•	Key Insights & Visuals:**

**-	Subcategory & Shipping Volume:** Ranks product subcategories by total orders **(led by Binders with 1,523 orders and Paper with 1,370)** and tracks order distribution across delivery classes **(Standard Class: 59.72%)**. 

**-	Seasonal Segment Trends:** Compares monthly product order volumes across Consumer, Corporate, and Home Office segments, showing peak demand in September, November, and December. 

**-	Geographic Decomposition Tree:** Provides an interactive drill-down of product orders from Region **(West: 3,203)** down to **State (California: 2,001)** and **City (Los Angeles: 747)**. 

**-	SKU Profitability Matrix:** Evaluates individual Product IDs by order count, quantity sold, revenue, net profit, and margin—using conditional formatting to flag both top earners **(e.g., TEC-CO-10004722 at 40.91% margin)** and unprofitable items **(TEC-MA-10000822 at -27.27%)**. 


### Page 4 – Order Analysis


<img width="1369" height="744" alt="Orders_Analysis" src="https://github.com/user-attachments/assets/f2b97b6d-2747-4d38-ae13-07a0e0b5a98a" />


**•	Purpose:** Focuses on order fulfillment dynamics, regional volume distribution, and weekly ordering patterns. 

**•	Key Metrics Tracked:** Highlights unique order counts (5,009 distinct orders across 38K total units sold) alongside core sales and margin KPIs, supported by a multi-city filter slicer. 

**•	Visual Breakdown:**

**-	Proportional Share (Donut Charts):** Displays order quantity distribution across Regions (West leads at 32.39%), Ship Modes (Standard Class at 60.19%), and Customer Segments (Consumer at 51.54%). 

**-	Day-of-Week Trends:** An area chart tracking daily order quantities across **Furniture, Office Supplies**, and **_Technology throughout_** the week. 

**-	Subcategory Demand:** Ranks top product subcategories by customer order volume, led by **Binders and Furnishings**. 


## 4. Headline KPIs

| KPI | Value |
|---|---|
| Total Sales | **$2,297,200.86** |
| Total Profit | **$286,397.02** |
| Sales Margin | **12.47 %** |
| Customers | **793** |
| Orders (distinct Order ID) | **5,009** |
| Order lines (rows) | **9,994** |
| Quantity sold | **37,873** |


## 5. Key insights


- **Growth:** sales rose from ~$484K (2014) to ~$733K (2017); profit from ~$50K to ~$93K.
- **Regions:** West leads in sales (~$725K) and margin (~14.9 %); Central is the weakest (~7.9 % margin).
- **Categories:** Technology (~17.4 %) and Office Supplies (~17.0 %) are highly profitable, while **Furniture returns only ~2.5 %**.
- **Loss makers:** **Tables** (≈ –$17.7K) and **Bookcases** (≈ –$3.5K) lose money overall; Texas and Pennsylvania are loss-making states despite strong sales.
- **Shipping:** Standard Class represents ~60 % of orders and ~57 % of profit.
- **Segments:** Consumer is ~52 % of orders, but Home Office has the best margin (~14 %).
- **Seasonality:** sales peak between September and December.

## 6. Recommendations

1. Review pricing and discount policy on **Tables, Bookcases and Furniture** in general.
2. Investigate the **Central region, Texas and Pennsylvania** (discounts, shipping cost, product mix).
3. Protect and grow top customers (e.g. Sean Miller, Tamara Chand, Raymond Buch) with loyalty offers.
4. Prepare stock and campaigns ahead of the **Q4 peak**.

## 7. Tools & skills

- **Power BI Desktop**: data modelling, DAX measures, slicers, decomposition tree, conditional formatting, map visuals, custom logo and layout
- **Power Query**: CSV import and transformation
- **Design**: consistent blue palette, KPI cards, 4-page navigation


## 8. Author

**Awono Jean Rodrigue** – Business Intelligence & Data Analyst, moving toward Data Engineering  

🔗 [LinkedIn](https://www.linkedin.com/) ·
