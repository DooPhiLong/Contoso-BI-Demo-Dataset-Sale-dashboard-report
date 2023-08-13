# 🏢 Contoso BI Demo Dataset Sale report
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-report/assets/120476961/99059d83-3617-433f-8dd6-6a296d1367e7)

## 💼 Business Case and Requirement

You are a Data Analyst working for an e-commerce company named X. You are tasked with preparing a presentation to present an overview of the company's business and operations to date for Sales and Operations Managers. 

### The presentation should include at a minimum the following information: 
- Sale business and products overview. 
- Demographics, customers overview.

### Some additional information for the case study:
- The business database based on The Contoso BI Demo dataset is used to demonstrate DW/BI functionalities across the entire Microsoft Office product family. This dataset includes C-level, sales/marketing, IT, and common finance scenarios for the retail industry and support map integration. In addition, this dataset offers large volumes of transactions from OLTP and well-structured aggregations from OLAP, along with reference and dimension data.
---

## 📂 Datasets
### Introduce about the dataset
- Database Contoso is an example database created by Microsoft to help learn and develop applications in the Microsoft SQL Server environment. It is used as a sample dataset to showcase Microsoft Business Intelligence products and DW/BI capabilities across the entire Microsoft Office product family.
- The dataset includes information about the company's departments such as C-levels, Sales/Marketing, IT, Finance and supports map integration, providing both OLTP (Online Transaction Processing) and OLAP (Online Analytical) data Processing), along with reference data and dimensions.
The Contoso database consists of tables such as Customer, Order, OrderDetail, and Product, each containing different information about the company's customers, orders, order details, and products. These tables have relationships with each other, allowing for complex and efficient data queries. For example, a customer can have many different orders, and each order can have many different line items.
- These data can be used for data analysis, visualization, and training of predictive and classification models. In education, Contoso is often used as an example to teach concepts in many areas such as databases, application development, and systems management.
- This database has a lot of tables showing data from different parts of the business system, but I have only pulled out a few tables below to do the required analysis, if you are interested in the dataset. Please visit this one [Here](https://www.microsoft.com/en-us/download/details.aspx?id=18279&44F86079-8679-400C-BFF2-9CA5F2BCBDFC=1)
### 📎 Orders dataset
Provide information about orders
- order_id: unique ID of the order
- customer_id: unique ID of the customer
- order_status: order status
- order_purchase_timestamp: time when the order was ordered
- order_approved_at: time the order is approved
- order_delivered_carrier_date: the time the item was delivered to the carrier
- order_delivered_customer_date: the time the item was delivered to the customer
- order_estimated_delivery_date: the estimated time the order will be delivered to the customer
#### Sample first 10 row of Orders dataset
![image](https://user-images.githubusercontent.com/120476961/229264008-449a687e-f4da-4af4-8e0b-761a8a1dd848.png)


### 📎 Order items dataset  
Provide information about each item in the order and shipping costs
- order_id: unique ID of the order
- order_item_id: ID of the item in the order (item number 1 has ID 1, item 2 has ID 2, etc. Based on this we also know how many items each order has)
- product_id: unique ID of the product in the order
- seller_id: unique ID of the seller
- price: the price of the item
- freight_value: shipping fee
#### Sample first 10 row of Order items dataset
![image](https://user-images.githubusercontent.com/120476961/229264066-ee559d5a-7e52-49cf-a2eb-a568e5554f1a.png)


### 📎 Order payments dataset
Provide information of order payments.
*Note that we need to combine all values of each order to have total values.*
- order_id: unique ID of order
- payment_sequential: sequence order
- payment_type: payment type
- payment_installments: full payment (payment_installments = 1) or installment (payment_installments > 1,total payment is splited to many payments .
- payment_value: payment value (payment_value - equal total payments of all times payment installments)
#### Sample first 10 row of Order payments dataset
![image](https://user-images.githubusercontent.com/120476961/229264148-77bb4ec3-46f8-47e2-a5ed-668df4d9e0ba.png)

### 📎 Product dataset 
Provide product information
- product_id: unique ID of product
- product_category_name: category product name 
- product_name_lenght: number of product name letters
- product_description_lenght: number of product description letters
- product_photos_qty: number of product photo
- product_weight_g: weight of product  (g)
- product_length_cm: length of product (cm)
- product_height_cm: height of product (cm)
- product_width_cm: width/deep of product (cm)
- product_category_name_english : category product name translated into English
#### Sample first 10 row of Product dataset 
![image](https://user-images.githubusercontent.com/120476961/229264279-3ed109da-b8a8-4539-838d-94042d771604.png)

### 📎 Order reviews dataset 
Provide review details of each order
- review_id: unique ID of revie
- order_id: unique ID of order
- review_score: Review Score
- review_comment_title: Comment title
- review_comment_message: detail of review
- review_creation_date: Created date of review
- review_answer_timestamp: timestamp of review answers
#### Sample first 10 row of Order reviews dataset 
![image](https://user-images.githubusercontent.com/120476961/229264314-c73b0b2c-e625-40b2-aec9-546a06c92073.png)

### 📎 Customers dataset
Provide Customer Information 

- customer_id: customer unique ID ( used to link with customer_id of orders_dataset table.
- customer_unique_id: unique ID of customer in system of customer information management. 
- customer_zip_code_prefix: zip code of customer
- customer_city: City name of customer 
- customer_state: State name of customer
#### Sample first 10 row of Customers dataset
![image](https://user-images.githubusercontent.com/120476961/229264328-c46ecdaf-2999-45be-9a82-528b9e127841.png)


## A. [Data Exploration and Cleaning by Power query](https://github.com/DooPhiLong/E-commerce-dashboard-report/blob/main/Data%20mining%20and%20cleaning.md)



## B. [Analysis](https://github.com/DooPhiLong/E-commerce-dashboard-report/blob/main/Analyst%20and%20dashboard%20report.md)

---

## 🔨 Method applied
- POWER QUERY
  - Data Exploration
  - Data cleaning
  - Data transformation
- POWER BI
  - Build data model
  - Visualize
  - Analyze
  - Dax fucntion
