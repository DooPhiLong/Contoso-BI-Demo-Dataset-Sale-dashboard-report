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

## 📌 Measure and Calculated columns by DAX

To support for anlysis chart, We need to create following Measure and Calculated columns by DAX : 
<details><summary> Click Here  </summary>

  
<details><summary> Add Full name column to DimCustomer dataset </summary>

```
Full name = CONCATENATE(DimCustomer[FirstName]&" ",CONCATENATE(DimCustomer[MiddleName]&" ",DimCustomer[LastName]))
```  
</details>  

<details><summary> Add Age column to DimCustomer dataset  </summary>

```
Age = DATEDIFF(DimCustomer[BirthDate],DATE(2007,12,31),YEAR)
```
</details>  

<details><summary> Calculate total cost </summary>

```
Total cost = SUM(FactSales[TotalCost])
  
```
</details>  

<details><summary> Calculate total sale </summary>

```
Total Sale = sum(FactSales[SalesAmount])
  
```  
</details>  

  
<details><summary> Calculate total profit </summary>

```
Total profit = [Total Sale] - [Total cost]
```
</details>  


<details><summary>  Calculate number of kind of products </summary>

```
Num kind of products = COUNT(DimProduct[ProductKey])
```
</details> 

<details><summary> Calculate number of products purchased </summary>

```
Num of products purchased = sum(FactSales[SalesQuantity])
```
</details>

<details><summary> Calculate number of products purchased   </summary>

```
Num of products returned = SUM(FactSales[ReturnQuantity])
```
</details>

<details><summary> Calculate number of customers   </summary>

```
Number of customers = COUNT(DimCustomer[CustomerKey])
```
</details>

<details><summary> Calculate number of returned customers   </summary>

```
Num of returned customers = COUNTROWS(FILTER(SUMMARIZE(FactSales,DimCustomer[CustomerKey],"Count",COUNTROWS(FactSales)),[Count] > 1 ))
```
</details>

<details><summary> Calculate number of Stores   </summary>

```
Num of Stores = COUNT(DimStore[StoreKey])
```
</details>

<details><summary> Calculate number of orders   </summary>

```
Number of orders = COUNT(FactSales[SalesKey])
```
</details>

<details><summary> Calculate profit percentage   </summary>

```
Per rev of Sale = [Total profit]/[Total Sale]
```
</details>

<details><summary> Calculate sales growth quarter-over-quarter   </summary>

```
Per sales quarter-over-quarter = 
    var Pre_quar_sales = CALCULATE([Total Sale],PREVIOUSQUARTER(DimDate[Date].[Date]))
    return ([Total Sale] - Pre_quar_sales)/Pre_quar_sales
```
</details>

<details><summary> Identify Rank of productsubcategory by product Quantity purchased   </summary>

```
Rank productsubcategory by product Quantity purchased = RANKX(ALL(DimProductSubcategory[ProductSubcategoryKey],DimProductSubcategory[ProductSubcategoryName]),[Num of products purchased])
```
</details>

<details><summary> Identify Rank of store by sale  </summary>

```
Rank store by sale = RANKX(ALL(DimStore[StoreKey],DimStore[StoreName]),[Total Sale])
```
</details>

<details><summary> Calculate Recent day's Sale   </summary>

```
Recent day's Sale = CALCULATE([Total Sale],LASTNONBLANK(DimDate[Date],[Total Sale]))
```
</details>

<details><summary> Calculate Recent month's Sale   </summary>

```
Recent month's Sale = Calculate([Total Sale],DimDate[MonthNumber] = MONTH(max(FactSales[DateKey])),DimDate[Year] = YEAR(max(FactSales[DateKey])))
```
</details>

<details><summary> Calculate Sale previous quarter   </summary>

```
Sale previous quarter = CALCULATE([Total Sale],PREVIOUSQUARTER(DimDate[Date].[Date]))
```
</details>

<details><summary> Calculate average area per Store   </summary>

```
AVG area per Store = Sum(DimStore[SellingAreaSize])/[Num of Stores]
```
</details>

<details><summary> Calculate average Cost per New Customer   </summary>

```
AVG Cost per New Customer = [Total cost]/([Number of customers] - [Num of returned customers])
```
</details>

<details><summary> Calculate average Cost per Store   </summary>

```
AVG Cost per Store = [Total cost]/[Num of Stores]
```
</details>

<details><summary> Calculate average Sale per Customer   </summary>

```
AVG Sale per Customer = [Total Sale]/[Number of customers]
```
</details>

<details><summary> Calculate average sale per order   </summary>

```
AVG sale per order = [Total Sale]/[Number of orders]
```
</details>

<details><summary> Calculate average sale per product   </summary>

```
AVG sale per product = [Total Sale]/[Num kind of products]
```
</details>

<details><summary> Calculate average Sale per Store   </summary>

```
AVG Sale per Store = [Total Sale]/[Num of Stores]
```
</details>

<details><summary> Calculate Cost per meters of store   </summary>

```
Cost per meters of store = [AVG Cost per Store]/[AVG area per Store]
```
</details>

<details><summary> Conditional statement to format the growth percentage  </summary>

```
Cond format growth per = IF ( [Per sales quarter-over-quarter] < 0, 1,IF(ISBLANK([Per sales quarter-over-quarter]),0,2))
```
</details>

</details>

## 📌 Data model

<details><summary> Click Here </summary>

![image](https://github.com/DooPhiLong/Contoso-BI-Demo-Dataset-Sale-report/assets/120476961/c4dbf852-f273-4b6e-ae32-df6f33862a6b)


</details>
