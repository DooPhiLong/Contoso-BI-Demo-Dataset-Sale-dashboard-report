# 🏢 Contoso BI Demo Dataset Sale report
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/c2157388-661d-45fd-9daa-65e83648b8f5)

## 💼 Business Case and Requirement

You are a Data Analyst working for an e-commerce company named X. You are tasked with preparing a presentation to present an overview of the company's business and operations to date for Sales and Operations Managers. 

### The presentation should include at a minimum the following information: 
- Sale business and Products, Store overview. 
- Demographics, customers overview.

### Some additional information for the case study:
- The business database based on The Contoso BI Demo dataset is used to demonstrate DW/BI functionalities across the entire Microsoft Office product family. This dataset includes C-level, sales/marketing, IT, and common finance scenarios for the retail industry and support map integration. In addition, this dataset offers large volumes of transactions from OLTP and well-structured aggregations from OLAP, along with reference and dimension data.
- Since this is a virtual database, numbers such as revenue, costs... are also symbolic. But it does not affect the mining process, data analysis and conclusions for the report
- The Sale bussiness in this case just run from 2007 to 2009.

## 📂 Datasets
### Introduce about the dataset
- Database Contoso is an example database created by Microsoft to help learn and develop applications in the Microsoft SQL Server environment. It is used as a sample dataset to showcase Microsoft Business Intelligence products and DW/BI capabilities across the entire Microsoft Office product family.
- The dataset includes information about the company's departments such as C-levels, Sales/Marketing, IT, Finance and supports map integration, providing both OLTP (Online Transaction Processing) and OLAP (Online Analytical) data Processing), along with reference data and dimensions.
The Contoso database consists of tables such as Customer, Order, OrderDetail, and Product, each containing different information about the company's customers, orders, order details, and products. These tables have relationships with each other, allowing for complex and efficient data queries. For example, a customer can have many different orders, and each order can have many different line items.
- These data can be used for data analysis, visualization, and training of predictive and classification models. In education, Contoso is often used as an example to teach concepts in many areas such as databases, application development, and systems management.
- If you are interested in the dataset. Please visit this one [Here](https://www.microsoft.com/en-us/download/details.aspx?id=18279&44F86079-8679-400C-BFF2-9CA5F2BCBDFC=1)
- This database has a lot of tables showing data from different parts of the business system, but I have only pulled out a few tables also attribute in table below to do the required analysis (I'm going to explant more clearly on **Data Preparation and Preprocessing part**)
### 📎 DimCustomer dataset
Provide information about customers
- CustomerKey : Unique ID of the customer
- FirstName : FirstName of the customer
- MiddleName : MiddleName of the customer
- LastName : LastName of the customer
- BirthDate : BirthDate of the customer
- Gender : Gender of the customer
- YearlyIncome : YearlyIncome of the customer
- Education : Education of the customer
- Occupation : Occupation of the customer
- Full name : Full name of the customer (This is calculated column. I'm going to explant more clearly on **Data preparation and Preprocessing part**)
- Age: Age of the customer (This is calculated column. I'm going to explant more clearly on **Data preparation and Preprocessing part**)
#### Sample first 10 row of DimCustomer dataset
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/e9634603-60f8-478f-ab13-4e50a54581f3)

### 📎 DimGeography dataset  
Provide information about each business area
- GeographyKey : Unique ID of the area
- GeographyType : Size of business area ( Country, Province, city....)
- ContinentName: Area's Continent name
- RegionCountryName : Area's  Region Country name
- StateProvinceName : Area's State Province name
- CityName : Area's City name
#### Sample first 10 row of DimGeography dataset 
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/6af45dff-bd3f-4d9e-928c-c0775f6adc14)


### 📎 DimProduct dataset
Provide information of Products
- ProductKey : Unique ID of Product
- ProductName : Product's Name
- ProductDescription : Product's Description
- ProductSubcategoryKey : To relate with DimProductSubcategory dataset, show Product's Category.
- BrandName : Peoduct's Brand name
- UnitCost : Product's cost
- UnitPrice : Product's price
#### Sample first 10 row of DimProduct dataset
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/dc00dbb8-ed53-48c2-95ab-b5afa7137c65)

### 📎 DimProductSubcategory dataset 
Provide information of Product Subcategorys
- ProductSubcategoryKey : Unique ID of Product Subcategory
- ProductSubcategoryName: Categoryproduct's name 
- ProductSubcategoryDescription : Categoryproduct's description
#### Sample first 10 row of Product dataset 
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/197a6329-220b-4283-8faf-97018e6d6425)


### 📎 Order DimPromotion dataset 
Provide review details of Promotions
- PromotionKey : Unique ID of Promotion
- PromotionName : Promotion's Name
- PromotionDescription : Promotion's Description
- DiscountPercent: Promotion's DiscountPercent
#### Sample first 10 row of DimPromotion dataset 
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/dffa7544-5dcb-4227-95d2-a405620d5769)


### 📎 DimStore dataset
Provide Information of Stores
- StoreKey : Unique ID of Store
- StoreName : Store's Name
- GeographyKey : To relate with DimGeography dataset, show Store's location
- StorePhone : Store's Phone
- StoreFax : Store's Fax
- AddressLine1 : Store's AddressLine1
- AddressLine2 : Store's AddressLine2
- SellingAreaSize : Store's AreaSize
#### Sample first 10 row of DimStore dataset
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/dd2d4016-c662-413a-95e0-905367b834b5)

### 📎 FactSales dataset
Provide detail information of Orders
- SalesKey : Unique ID of Order
- DateKey : Time the order takes place
- CustomerKey :To relate with DimCustomer dataset, show who customer this order belongs to
- StoreKey : To relate with DimStore dataset, show which store this order belongs to
- ProductKey : To relate with DimProduct dataset, show which products this order has
- PromotionKey : To relate with DimPromotion dataset, show which promotion this order applied
- UnitCost : Porduct'unit cost
- UnitPrice : Porduct'unit price
- SalesQuantity : Product's quantity
- ReturnQuantity : Product returned's quantity
- ReturnAmount : Product returned's Amount
- DiscountQuantity : Discount's quantity
- DiscountAmount : Discount's amount
- TotalCost : Order's total cost
- SalesAmount : Order's Sale amount
#### Sample first 10 row of FactSales dataset
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/1dce69e5-f153-430d-a29a-eda4e6503cbd)

## A. [Data Preparation and Preprocessing](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-dashboard-report/blob/main/Data%20preparation%20and%20Preprocessing.md)
## B. [Analysis](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/blob/main/Analytic%20and%20Dashboard%20report.md)

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
- SQL Server
  - database storage
