# AdventureWorks Sales Analytics End-to-End Project

## Overview

This project demonstrates an end-to-end Business Intelligence and Analytics solution using Microsoft's AdventureWorks dataset.

The project follows a real-world analytics workflow used by Data Analysts, Power BI Developers, and BI Engineers, covering data profiling, data transformation, data modeling, dashboard development, and documentation.

---

## Project Objectives

- Perform data profiling using Python and Pandas.
- Build reusable ETL processes.
- Create a dimensional star schema model.
- Design SQL-based analytical structures.
- Develop interactive Power BI dashboards.
- Document the complete analytics lifecycle using GitHub.

---

## Dataset

### Source

Microsoft AdventureWorks Dataset

### Available Files

#### Fact Tables

- AdventureWorks Sales Data 2020
- AdventureWorks Sales Data 2021
- AdventureWorks Sales Data 2022
- AdventureWorks Returns Data

#### Dimension Tables

- AdventureWorks Customer Lookup
- AdventureWorks Product Lookup
- AdventureWorks Product Categories Lookup
- AdventureWorks Product Subcategories Lookup
- AdventureWorks Territory Lookup
- AdventureWorks Calendar Lookup

---

## Project Architecture

```text
AdventureWorks CSV Files
          │
          ▼
    Python ETL Layer
    (Pandas & NumPy)
          │
          ▼
     FactSales Table
          │
          ▼
       SQL Model
          │
          ▼
      Power BI Model
          │
          ▼
Interactive Dashboards
          │
          ▼
Business Insights
```

---

## Technology Stack

| Technology | Purpose |
|------------|----------|
| Python | Data Profiling & ETL |
| Pandas | Data Transformation |
| NumPy | Numerical Operations |
| SQL | Data Modeling |
| Power BI | Data Visualization |
| Git | Version Control |
| GitHub | Documentation & Collaboration |

---

## Project Structure

```text
AdventureWorks-Sales-Analytics
│
├── Data
│   ├── Raw
│   └── Processed
│
├── docs
│   ├── Data_Source.md
│   ├── Data_Model.md
│   ├── Data_Dictionary.md
│   └── ETL_Journey.md
│
├── python
│   ├── merge_sales_data.ipynb
│   └── merge_sales_data.py
│
├── sql
│
├── PowerBI
│
├── README.md
└── LICENSE
```

---

## Data Model

### FactSales

Contains sales transactions from:

- 2020
- 2021
- 2022

Key Fields:

- orderdate
- productkey
- customerkey
- territorykey
- orderquantity

---

### FactReturns

Contains product return transactions.

Key Fields:

- returndate
- productkey
- territorykey
- returnquantity

---

### Dimensions

#### DimCustomer

Customer demographics including:

- Annual Income
- Occupation
- Education Level
- Home Owner Status

#### DimProduct

Product master information including:

- Product Name
- Product Category
- Product Subcategory
- Product Cost
- Product Price

#### DimTerritory

Geography hierarchy:

- Region
- Country
- Continent

---

## ETL Process

### Phase 1: Data Profiling

Completed:

- Load datasets using Pandas
- Validate schema
- Validate data types
- Check null values
- Check duplicate records
- Convert date fields
- Validate yearly transaction ranges

### Phase 2: Data Standardization

Completed:

- Column name standardization
- Datetime conversion
- Reusable standardization function

### Phase 3: Data Consolidation

Planned:

- Merge 2020 Sales Data
- Merge 2021 Sales Data
- Merge 2022 Sales Data
- Create FactSales dataset

---

## Planned SQL Deliverables

- Data Profiling Queries
- Fact Table Design
- Dimension Table Design
- Analytical Views
- KPI Calculations

---

## Planned Power BI Deliverables

### Executive Dashboard

KPIs:

- Total Orders
- Order Quantity
- Return Quantity
- Return Rate

### Product Analytics

- Product Performance
- Category Analysis
- Subcategory Analysis

### Customer Analytics

- Customer Segmentation
- Income Analysis
- Occupation Analysis

### Geography Analytics

- Regional Performance
- Country Analysis
- Territory Analysis

### Time Intelligence

- Year-over-Year Growth
- Monthly Trends
- Quarterly Performance

---

## Author

Deepak Janaparapu

Senior Analyst | SQL | Python | Power BI | Data Analytics

---

## License

This project is licensed under the MIT License.
