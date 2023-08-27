# Power-BI-Olist-E-commerce-Sales-and-Logistics-Performance-Analysis
This project used the order data set from an e-commerce platform to develop a dashboard describing the sales and logistics  performance.

1. About the company:

Olist, founded in 2015 by Tiago Dalvi in Curitiba, Brazil, is an e-commerce platform connecting sellers and products to Brazil's main markets. It boasts over 200,000 users in 180 countries and serves 45,000+ shop owners and retailers.

2. About dataset:

This dataset contains 100,000 orders from Olist Store in Brazil, spanning 2016 to 2018. It covers various aspects of orders, including status, price, payment methods, shipping, product details, and customer reviews. Geolocation data with latitude and longitude coordinates for Brazilian zip codes is also included. Note that sensitive information has been anonymized for security.

3. Backgroud:

This dataset is from Olist, a leading Brazilian department store that connects small businesses across the country to various sales channels through a single contract. Sellers can list products on Olist, which handles logistics. Once a customer orders a product, the seller is notified to fulfill it. After delivery, customers receive a satisfaction survey via email to provide feedback on their buying experience. Visit www.olist.com for more information.
Attention
- An order can have many items.
- Each item can be made by a separate seller.
- All information about stores and partners has been replaced with another name
to keep information confidential, but not to affect the following data processing

4. Data dictionary:

orders table:
- order_id: Order ID (numeric)
- Country_id: Country ID (numeric)
- Order_status: Order status (categorical string)
- order_purchase_timestamp: Time when the order was created/ordered (datetime)
- order_approved_at: Time to receive and process orders (datetime)
- order_delivered_carrier_date: Time to delivery orders (datetime)
- order_delivered_customer_date: The actual time the buyer receives the goods (datetime)
- order_estimated_delivery_date: Estimated time the buyer will receive the goods (datetime)
order_items table:
- order_id: Order ID (numeric)
- order_item_id: Order number of the product in the order (numeric)
- product_id: Product ID (numeric)
- seller_id: Seller ID (numeric)
- shipping_limit_date: Shipping limit date (datetime)
- price: Product price (numeric)
- freight_value: Shipping price (numeric)

order_payment table:
- order_id: Order ID (numeric)
- payment_sequential: Payment sequential (numeric)
- payment_type: Payment Type (numeric)
- payment_installments: Payment installation (for credit card) (categorical string)
- payment_value: Payment value (numeric)

product_category_name_translation table:
- product_category_name: Product category name (categorical string)
- product_category_name_english: Product English category name (categorical string)

seller table:
- seller_id: Seller ID (numeric)
- seller_zip_code_prefix: Seller's zipcode (numeric)
- seller_city: Seller's city (categorical string)
- seller_state: Seller's state (categorical string)

products table:
- product_id: Product ID (numeric)
- product_category_name: Product category name(categorical string)
- product_name_length: Product name length (numeric)
- product_description_length: Product description length (numeric)
- product_photos_qty: Product photos quantity (numeric)
- product_weight_g: Product weight (numeric)
- product_length_cm: Product length (numeric)
- product_height_cm: Product height (numeric)
- product_width_cm: Product width (numeric)

5. Methodology:

- Data Preparation: Created “dim_date” table using ADDCOLUMNS + CALENDAR (DAX functions) → optimize the time of fact
table; created “Quantity” column based on given columns to make “Order_ID” column become unique.
- Data Modeling: used Dimensional Data Modeling method involving fact and dimension tables (linked by Primary and Foreign 
keys).
- Visualization techniques: The dashboard is developed into 2 parts: Sales Performance & Logistics Performance; Line, bar, pie, 
stacked charts, cards, and slicers are used to present data performance and comparison.

6. Analysis Process:

- Build Data Model
- Data Cleaning and Standardizing
- Develop dashboard and contribute conclusions.

7. Analytics Requests:

• Used DAX functions to calculate performance metrics such as #Revenue, #Quantity, #Product, #Sellers, #Freight Value, AVG
Delivered Days, AVG Product Weight, AVG Product Volume,…
• Used different types of charts to compare performance under different dimensions such as Time, Payment Type, Area, 
Category, Seller, Status,…
• Used Slicers to get deeper view into performance such as Time, Product Categories, States slicers.
