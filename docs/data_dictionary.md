# Data Dictionary

## FactSales

| Column | Description |
|----------|------------|
| OrderNumber | Unique order identifier |
| OrderDate | Date of the transaction |
| ProductKey | Product identifier |
| CustomerKey | Customer identifier |
| TerritoryKey | Sales territory identifier |
| OrderQuantity | Quantity sold |
| SalesAmount | Revenue generated |

---

## FactReturns

| Column | Description |
|----------|------------|
| ProductKey | Product identifier |
| TerritoryKey | Sales territory |
| ReturnQuantity | Quantity returned |

---

## DimCustomer

| Column | Description |
|----------|------------|
| CustomerKey | Unique customer identifier |
| FirstName | Customer first name |
| LastName | Customer last name |
| Occupation | Customer occupation |
| Gender | Customer demographic attribute |
| AnnualIncome | Customer annual income |

---

## DimProduct

| Column | Description |
|----------|------------|
| ProductKey | Unique product identifier |
| ProductName | Product name |
| ProductSubcategoryKey | Product subcategory |
| ProductCategoryKey | Product category |
| ProductCost | Product cost |

---

## DimTerritory

| Column | Description |
|----------|------------|
| TerritoryKey | Unique territory identifier |
| Region | Sales region |
| Country | Country |
| Continent | Continent |

---

## DimDate

| Column | Description |
|----------|------------|
| Date | Calendar date |
| Year | Calendar year |
| Quarter | Calendar quarter |
| Month | Calendar month |
