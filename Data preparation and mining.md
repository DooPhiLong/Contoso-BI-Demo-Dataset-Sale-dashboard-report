# Data mining and cleaning

Because this is a virtual database created from Microsoft to support the practice of analysis. So the data from the tables are mostly cleaned and there are no errors in data such as formatting, spelling, meaning, and especially empty cells have their own meaning, not due to missing data
## 🔨 Tool : SQL sever, Power BI and Power query 
## 📌 Add DATA from SQL sever to Power BI
<details><summary> Step 1 </summary>
Connect with SQL sever database
  
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/8baf5254-1774-450a-ac97-d93173a3ba1f)
</details>
<details><summary> Step 2 </summary>
Pick out any necessary dimensions for analytic
  
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/96d7c367-733a-4f86-9e2f-7c8e959ff4c3)
</details>

## 📌 CLEAN and TRANSFORM DATA (Power query)
### 📎 DimCustomer dataset
- There are 3 things I would check in DimCustomer dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
  - Explain why keep or drop the null values
 <details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>
<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/3a720b49-7a83-409a-9ff5-8a5217cdf01d)
</details>

<details><summary>  Explain why keep or drop the null values  </summary>

- I kept the null values in the MiddelName columns because It is normal there are customers who don't have middle names
</details>

---
### 📎 DimGeography dataset
- There are 3 things I would check in DimGeography dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
  - Explain why keep or drop the null values
  - 
<details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>

<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/a9ae1962-abbe-4d76-a5d6-db2a6dfdda2f)

</details>

<details><summary>  Explain why keep or drop the null values  </summary>

- I kept the null values in the CityName, StateProvinceName, RegionCountryName columns Because there are many scale business models across different administrative hierarchies. For example, the first line is hierarchical by continent, obviously this business model does not belong to any country, so the columns of country, province, and city names are null.
</details>

---
### 📎 DimProduct dataset
- There are 2 things I would check in DimProduct dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
<details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>

<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/439d7c83-f3f3-4ae5-878c-b75e7f2f8394)
</details>
 
---
### 📎 DimProductSubcategory Dataset

- There are 2 things I would check in DimProductSubcategory dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
<details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>

<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/18ca05d7-94af-446b-aa3a-de317955d07e)

</details>

---
### 📎 DimPromotion Dataset
- There are 2 things I would check in DimPromotion dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
<details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>

<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/10f32254-7d62-4d58-983a-9baf1d273946)
</details>



---  
### 📎 DimStore Dataset
- There are 3 things I would check in DimStore dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
  - Explain why keep or drop the null values
 <details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>
<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/ded52902-c13e-4973-abe8-4134a007846c)

</details>

<details><summary>  Explain why keep or drop the null values  </summary>

- I kept the null values in the AddressLine1 column and AddressLine2 column because It show that store are not officially put into operation yet
</details>

---
### 📎 FactSales  Dataset
- There are 3 things I would check in DimStore dataset:
  - Remove columns that not necessary for analytic, just keep any columns I showed below in the **overall info** part
  - The overall info
 <details><summary>  Remove columns that not necessary for analytic  </summary>
   
- Right click on the columns that i want to remove and click into Remove 
</details>
<details><summary> Overall infomation </summary>
  
  - First sample 10 rows
  - Checking distinct, unique, error, empty values
![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/df62948a-a1b6-448c-b849-b2c57d663a9b)
</details>

---

## 📌 Measure and Calculated columns

To support for anlysis chart, We need to create following Measure and Calculated columns by DAX : 
<details><summary> Add Review score column to order_items_dataset (related with review_score column of order_reviews_dataset)   </summary>

```
Review score = LOOKUPVALUE(order_reviews_dataset[review_score],order_reviews_dataset[order_id],order_items_dataset[order_id])
```  
![image](https://user-images.githubusercontent.com/120476961/235682271-38865fa1-7500-4f7a-9a94-91d36af5892c.png)
</details>  

<details><summary> Add comment column to order_reviews_dataset (show that order has comment or not)  </summary>

```
Comment = if(order_reviews_dataset[review_comment_message] = BLANK(),"No comment","Comment")
  
```
![image](https://user-images.githubusercontent.com/120476961/235682673-bdce1cbb-5915-47f6-b942-58a7f3fb4c7b.png)

</details>  

<details><summary> Split month and year from order_delivered_customer_date column of orders_dataset table to two column </summary>

```
Month_delivered_customer_date = MONTH(orders_dataset[order_delivered_customer_date])
Year_delivered_customer_date = YEAR(orders_dataset[order_delivered_customer_date])
  
```
![image](https://user-images.githubusercontent.com/120476961/235683039-c8455168-34bc-48e7-8431-5dbd35b0c292.png)

</details>  

<details><summary> Split hour from order_purchase_timestamp column of orders_dataset table to a column </summary>

```
Hour purchase timestamp = HOUR(orders_dataset[order_purchase_timestamp])
  
```
![image](https://user-images.githubusercontent.com/120476961/235683105-976c879a-e44d-4ee1-8551-9daea07740a4.png)

</details>  

<details><summary> calculate the total time that each order is delivered to the customer </summary>

```
Total time to receive the goods = DATEDIFF(orders_dataset[order_purchase_timestamp],orders_dataset[order_delivered_customer_date],DAY)
  
```
![image](https://user-images.githubusercontent.com/120476961/235683172-86b4ca03-fc18-4fe7-a39b-012f8a5076a3.png)

</details>  

<details><summary> Count of Orders </summary>

```
Count of Orders = COUNT(orders_dataset[order_id])
  
```  
</details>  

  
<details><summary> Count of product </summary>

```
Count of product = count(order_items_dataset[product_id])
```
</details>  


<details><summary>  Count of comments  </summary>

```
Count of comment orders = COUNTROWS(FILTER(order_reviews_dataset,order_reviews_dataset[Comment] = "Comment"))
```
</details> 

<details><summary> Average review score   </summary>

```
Average review score = DIVIDE(SUM(order_reviews_dataset[review_score]), COUNT(order_reviews_dataset[review_score]))
```
</details>

<details><summary> Amount of orders previous month   </summary>

```
Orders_previous_month = 
CALCULATE([Count of Orders],
FILTER(ALLSELECTED(orders_dataset),
    if(max(orders_dataset[Month_delivered_customer_date]) = 1, 

        orders_dataset[Year_delivered_customer_date] = max(orders_dataset[Year_delivered_customer_date]) - 1
        &&
        orders_dataset[Month_delivered_customer_date] = 12, 

        orders_dataset[Year_delivered_customer_date] = max(orders_dataset[Year_delivered_customer_date])
        &&
        orders_dataset[Month_delivered_customer_date] = max(orders_dataset[Month_delivered_customer_date]) -1)))
```
</details>

<details><summary> Growth percentage monthly   </summary>

```
Growth percentage = DIVIDE(([Count of Orders]-[Orders_previous_month]),[Orders_previous_month])
```
</details>

<details><summary> Conditional statement to format the growth percentage  </summary>

```
Cond format growth per = IF ( [Growth percentage] < 0, 1,IF(ISBLANK([Growth percentage]),0,2))
```
</details>

<details><summary> Ranking amount of product category has sold  </summary>

```
Rank cate = RANKX(ALL(product_summarize_dataset[product_category_name_english]),[Count of product],,DESC,Dense)
```
</details>

## 📌 Data model

<details><summary> Click Here  </summary>

![image](https://user-images.githubusercontent.com/120476961/229851073-2f60ca70-b7ac-43af-9c37-fc629b137901.png)

</details>
