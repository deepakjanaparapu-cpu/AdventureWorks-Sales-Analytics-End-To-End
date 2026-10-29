# ETL Specification

## Objective

Consolidate AdventureWorks sales data into a single FactSales dataset.

## Source Files

- AdventureWorks Sales Data 2020.xlsx
- AdventureWorks Sales Data 2021.xlsx
- AdventureWorks Sales Data 2022.xlsx

## Target Output

FactSales.csv

## ETL Steps

### Extract

Read sales data from all source files.

### Transform

- Standardize column names
- Validate data types
- Check for duplicates
- Check for null values
- Append datasets

### Load

Export consolidated dataset into:

data/processed/FactSales.csv

## Quality Checks

- Validate row counts
- Validate date ranges
- Check duplicate sales records
- Verify sales amount totals

## Expected Deliverable

Single FactSales dataset containing all sales transactions from 2020 through 2022.
