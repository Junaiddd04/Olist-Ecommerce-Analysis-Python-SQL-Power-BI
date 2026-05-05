# Olist E-Commerce: End-to-End Sales & Logistics Analytics<br><br>
# Project Overview<br>
This project is an end-to-end data analytics pipeline analyzing over 100,000 transaction records from Olist, a Brazilian e-commerce platform. The goal was to transform highly fragmented raw data into a structured relational database and build an interactive dashboard to uncover actionable business insights regarding revenue drivers and logistical bottlenecks.


# Data Architecture & Tech Stack<br>
This project maps the entire lifecycle of an e-commerce transaction through a robust data pipeline:

## Data Cleaning & Preprocessing (Python / Pandas):<br>

Resolved complex many-to-many duplication traps by leveraging order_item_id.

Safely aggregated transactional payment data to prevent artificial revenue inflation.

Handled missing geographic coordinates by imputing state-level averages to preserve critical sales records.

## Database Modeling (MySQL):<br>

Used SQLAlchemy to push cleaned Python DataFrames directly into a structured MySQL database.

Engineered a highly optimized Star Schema, centralizing the ecommerce_sales Fact table surrounded by Dimension tables (Customers, Products, Sellers, Geolocation).

Data Visualization & Analytics (Power BI):

Built advanced DAX measures to handle dynamic filter contexts.

Engineered custom KPI logic to calculate lifetime repeat customer rates and accurate average delivery times while ignoring nulls from canceled orders.

# Dashboard Previews
<img width="1324" height="739" alt="Screenshot 2026-04-25 101516" src="https://github.com/user-attachments/assets/2ac69bae-00d8-4dd8-84e0-42f2a65883c8" />
<img width="1322" height="738" alt="Screenshot 2026-04-25 101539" src="https://github.com/user-attachments/assets/b3cf943e-0664-420d-b2e6-8c6fbbf082b3" />

1. Sales Performance
(Highlighting revenue trends, top-performing states, and high-value product categories)

2. Shipping & Reviews
(Visualizing the impact of logistics on customer satisfaction and mapping freight inefficiencies)

# Key Business Insights<br>
## The Cost of Delivery Delays<br>
While 92.26% of orders are delivered on time, the 7.74% that are delayed severely damage brand reputation.

On-time deliveries yield 78% positive reviews and only 13% negative reviews.

Delayed deliveries cause negative reviews to instantly spike to 53%, while positive reviews crash to 33%.

## Geographic Freight Inefficiencies<br>
Product weight has a surprisingly weak correlation with shipping costs. Geography is the primary driver. Customers in remote northern states (RR, PB, RO) pay nearly 3x higher freight costs (~$41–$43) compared to buyers in central hubs like São Paulo (~$15).

## High-Volume vs. High-Value Categories<br>
Bed, Bath & Table drives the highest order volume (11.2K orders).

Computer Accessories, however, acts as the primary cash cow. Despite having fewer orders (7.9K), it generates the second-highest total revenue ($1.59M), indicating a highly profitable premium pricing tier.

## Strategic Recommendations<br>
Automate Delay Management: Knowing that a delay quadruples negative reviews, Olist must implement automated CRM workflows. When an order passes its estimated delivery date, automatically issue an apology and a discount code to intercept the negative review.

Optimize Remote Freight: To remain competitive in northern states, Olist should consider localized micro-fulfillment centers or renegotiated bulk shipping rates for the RR, PB, and RO routes.

Protect High-Value Freight: Since heavy items show a higher probability of delay, partner with specialized heavy-freight carriers rather than standard postal services to protect the customer experience for high-ticket items like Furniture & Decor.


## Contact<br>
If you have any questions or feedback, feel free to reach out!

LinkedIn: www.linkedin.com/in/mohd-junaiddd04
