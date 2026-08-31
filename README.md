# Olist E-Commerce Data Analysis

## Project Overview

This project provides a deep dive into the Olist Brazilian E-Commerce dataset. It covers the entire customer journey, from order placement and payment to delivery and customer reviews. The analytical goal is to evaluate sales performance, geographic distribution of orders, delivery efficiency, and customer satisfaction.

## Dataset

The dataset consists of multiple related Excel files detailing different aspects of the e-commerce business.

- **Datasets Included:**
  - `olist_customers_dataset.xlsx`
  - `olist_orders_dataset.xlsx`
  - `olist_order_items_dataset.xlsx`
  - `olist_order_payments_dataset.xlsx`
  - `olist_order_reviews_dataset.xlsx`
  - `olist_products_dataset.xlsx`
  - `olist_sellers_dataset.xlsx`
  - `product_category_name_translation.xlsx`
- **Important Fields/Columns:** order_id, customer_id, product_id, price, freight_value, payment_value, review_score, order_status, order_purchase_timestamp.
- **Main Dimensions:** Time (Year, Month), Location (State, City), Product Category.
- **Main Measures:** Total Price, Freight Price, Order Count, Payment Value, Review Score.

## Data Analysis

The project leverages comprehensive data modeling and visualization techniques:
- **Data Modeling:** Establishing relationships between various datasets (Orders, Customers, Products, Reviews, Payments).
- **Pivot Tables & Charts:** Extensive use of pivots to summarize data by year, month, state, and product.
- **Calculated Fields & KPIs:** Generating overarching business metrics.
- **Geographic Analysis:** Mapping sales and freight costs across Brazilian states.
- **Customer & Product Analysis:** Analyzing top products, review scores, and payment methods.
- **Trend Analysis:** Tracking sales and product volume over time.

---

## Dashboard 1 — Home Overview

### Dashboard Overview
The Home dashboard acts as the executive summary, providing high-level KPIs and tracking overall financial performance over time.

### KPIs
- **Customer (99441):** Total unique customers.
- **Sellers (112650):** Total sellers involved.
- **Orders (99441):** Total number of orders placed.
- **Payment Value ($16,008,872.12):** Total value processed through payments.
- **Total Price ($13,591,643.70):** Total revenue from products.
- **Total Freight ($2,251,909.54):** Total shipping costs.
- **Ave.Freight ($19.99):** Average freight cost per order.
- **Ave.Review (4.1):** Average customer review score (out of 5).

### Filters & Slicers
- Built-in navigation buttons to move between 'Home', 'Order', 'Location', 'Rate', and 'Pivot'.

### Visualizations
- **Total Price Trend (Line Chart):** Tracks the total product revenue over time (Sept 2016 to Sept 2018), showing significant growth throughout 2017.
- **Top 10 Of Product (Bar Chart):** Displays the highest-grossing product categories, with 'beleza_saude' (health & beauty) leading.
- **Order Per Year (Pie Chart):** Breaks down the proportion of orders by year (2016, 2017, 2018).
- **Payment Type (Pie Chart):** Shows the distribution of payment methods, with 'credit_card' being the most dominant.

### Key Insights
- Total revenue experienced a strong upward trend from early 2017 into 2018.
- Credit cards are by far the preferred payment method.
- Health & beauty ('beleza_saude') and watches/gifts ('relogios_presentes') are the top revenue-generating categories.

<div align="center">
  <img src="https://github.com/elkrdawy111/Excel_analysis_photos/blob/main/olist/home.png?raw=true" alt="Excel Dashboard Overview" width="800"/>
</div>

<br>

---

## Dashboard 2 — Order Analysis

### Dashboard Overview
The Order dashboard focuses on product movement, delivery statuses, and freight costs relative to product weight.

### Filters & Slicers
- **State Slicer:** Filter metrics by specific Brazilian states (AC, AL, AM, etc.).
- **Product Slicer:** Filter by specific product categories.

### Visualizations
- **Count of Product Per Month (Stacked Bar Chart):** Shows the volume of products sold each month, broken down by year (2017 vs 2018).
- **Freight_Price Per Weight (Line & Area Chart):** Compares the average weight of items against the average freight price. It highlights that freight costs increase significantly with product weight.
- **Rate Per Date (Line Chart):** Tracks the average customer review score over time, maintaining a steady average near 4.0.
- **Order Status (Horizontal Bar Chart):** Displays the current status of all orders. The vast majority are 'delivered'.
- **Product Category (Bar Chart):** Shows the total count of items sold per category, with 'cama_mesa_banho' (bed, bath, table) being the most frequently ordered by volume.

### Key Insights
- Order volumes peaked heavily in November (likely Black Friday sales).
- The delivery success rate is extremely high, as almost all tracked orders are marked 'delivered'.
- While 'health & beauty' generates the most revenue (Home dashboard), 'bed, bath & table' items sell the highest quantity.
<div align="center">
  <img src="https://github.com/elkrdawy111/Excel_analysis_photos/blob/main/olist/order.png?raw=true" alt="Excel Dashboard Overview" width="800"/>
</div>

<br>

## Dashboard 3 — Location Analysis

### Dashboard Overview
The Location dashboard provides a geographic perspective on sales, focusing on which states and cities generate the most revenue and orders, as well as geographic freight disparities.

### Filters & Slicers
- **Product Slicer:** Filter geographic data by product category.

### Visualizations
- **Freight Per State (Pie Chart):** Shows the distribution of total freight costs among the top states (SP, RJ, MG, etc.).
- **Seller Per City & Freight Per City (Pie Charts):** Analyzes the concentration of sellers and freight costs in major cities (e.g., SP, curitiba).
- **Freight Per State (Line Chart):** Compares the average freight cost across different states, highlighting that some states (e.g., PB, RO) have significantly higher shipping costs.
- **Order Per State (Bar Chart):** Ranks states by order volume over different years. SP (São Paulo) dwarfs all other states.
- **Price Per State (Horizontal Bar Chart):** Ranks states by total revenue. SP, RJ, and MG are the top three.

### Key Insights
- São Paulo (SP) is the undisputed center of this e-commerce ecosystem, leading massively in both order volume and total revenue.
- Freight costs vary significantly by state, posing a potential barrier to sales in remote regions with higher averages.
- 
<div align="center">
  <img src="https://github.com/elkrdawy111/Excel_analysis_photos/blob/main/olist/location.png?raw=true" alt="Excel Dashboard Overview" width="800"/>
</div>

<br>

## Dashboard 4 — Rating & Review Analysis

### Dashboard Overview
The Rate dashboard investigates customer satisfaction, focusing on review scores, delivery times, and the correlation between the two.

### KPIs
- **Approved (2):** Orders in approved status.
- **Canceled (625):** Canceled orders.
- **Created (5):** Newly created orders.
- **Delivered (96478):** Successfully delivered orders.
- **Invoiced (314):** Invoiced orders.
- **Processing (301):** Orders being processed.
- **Shipped (1107):** Orders in transit.
- **Unavailable (609):** Unavailable orders.
- **Day Delivered (11.02):** Average number of days taken to deliver an order.

### Visualizations
- **Reviews Over Time (Line Chart):** Tracks average review scores month-by-month. The score dipped significantly in late 2016 but stabilized around 4.1 thereafter.
- **Review Scores Histogram (Bar & Line Chart):** Shows the distribution of review scores (1 to 5). The vast majority of customers leave a 5-star review, though there is a noticeable spike in 1-star reviews compared to 2, 3, or 4 stars.
- **Average Delivery (Line Chart):** Tracks the average delivery time over the months. Delivery times spiked in late 2016 and early 2018.
- **Delivery Time vs Review Score Scatter Plot:** Plots individual review scores against delivery days.

### Key Insights
- The average delivery time is approximately 11 days.
- Customer satisfaction is polarized: customers generally either give a perfect 5-star review or a 1-star review, with fewer moderate ratings in between.
- Periods with spikes in average delivery times loosely correlate with dips in average review scores.

<div align="center">
  <img src="https://github.com/elkrdawy111/Excel_analysis_photos/blob/main/olist/rate.png?raw=true" alt="Excel Dashboard Overview" width="800"/>
</div>

<br>
