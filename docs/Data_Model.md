# Data Model Design

## Model Type

Star Schema

## Fact Tables

### FactSales

Source Files:
- AdventureWorks Sales Data 2020
- AdventureWorks Sales Data 2021
- AdventureWorks Sales Data 2022

Measures:
- Sales Amount
- Order Quantity
- Revenue

### FactReturns

Source File:
- AdventureWorks Returns Data

Measures:
- Return Quantity

---

## Dimension Tables

### DimCustomer

Source:
- AdventureWorks Customer Lookup

Key:
- CustomerKey

Attributes:
- Customer Name
- Annual Income
- Occupation
- Education
- Gender

---

### DimProduct

Source:
- AdventureWorks Product Lookup

Key:
- ProductKey

Attributes:
- Product Name
- Product Category
- Product Subcategory

---

### DimDate

Source:
- AdventureWorks Calendar Lookup

Key:
- Date

Attributes:
- Year
- Quarter
- Month
- Day

---

### DimTerritory

Source:
- AdventureWorks Territory Lookup

Key:
- TerritoryKey

Attributes:
- Region
- Country
- Continent

---

## Relationship Design

DimCustomer 1 -> * FactSales

DimProduct 1 -> * FactSales

DimDate 1 -> * FactSales

DimTerritory 1 -> * FactSales

DimProduct 1 -> * FactReturns

---

## Planned KPIs

- Total Sales
- Total Orders
- Total Returns
- Return Rate %
- Total Customers
- Average Order Value
- Top Products
- Top Territories
- Year-over-Year Growth
