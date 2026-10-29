# AdventureWorks Sales Data 2020

## Step 1: Import Libraries

### Code

```python
import pandas as pd
import numpy as np
```

### Purpose

Import libraries required for data analysis and transformation.

---

## Step 2: Load Dataset

### Code

```python
sales_2020 = pd.read_csv(
    "../Data/Raw/AdventureWorks Sales Data 2020.csv"
)
```

### Purpose

Load the AdventureWorks Sales Data 2020 dataset into a Pandas DataFrame.

### Learning

The dataset was successfully loaded from the Raw data directory.

---

## Step 3: Preview Dataset

### Code

```python
sales_2020.head()
```

### Purpose

Inspect the first five records.

### Outcome

Verified successful file load and reviewed dataset structure.

---

## Step 4: Validate Dataset Dimensions

### Code

```python
sales_2020.shape
```

### Result

```python
(2630, 8)
```

### Finding

- Total Rows: 2630
- Total Columns: 8

---

## Step 5: Review Column Names

### Code

```python
sales_2020.columns
```

### Finding

- OrderDate
- StockDate
- OrderNumber
- ProductKey
- CustomerKey
- TerritoryKey
- OrderLineItem
- OrderQuantity

---

## Step 6: Standardize Column Names

### Code

```python
sales_2020.columns = sales_2020.columns.str.lower()
```

### Transformation

| Original | Standardized |
|----------|----------|
| OrderDate | orderdate |
| StockDate | stockdate |
| OrderNumber | ordernumber |
| ProductKey | productkey |
| CustomerKey | customerkey |
| TerritoryKey | territorykey |
| OrderLineItem | orderlineitem |
| OrderQuantity | orderquantity |

### Purpose

Improve consistency and simplify coding.

---

## Step 7: Review Data Types

### Code

```python
sales_2020.dtypes
```

### Finding

Date columns were initially loaded as strings.

---

## Step 8: Validate Missing Values

### Code

```python
sales_2020.isnull().sum()
```

### Finding

No significant missing values identified.

---

## Step 9: Validate Duplicate Records

### Code

```python
sales_2020.duplicated().sum()
```

### Result

```python
0
```

### Finding

No duplicate records found.

---

## Step 10: Convert Date Columns

### Code

```python
sales_2020['orderdate'] = pd.to_datetime(
    sales_2020['orderdate']
)

sales_2020['stockdate'] = pd.to_datetime(
    sales_2020['stockdate']
)
```

### Purpose

Convert string values to datetime format for analysis.

### Outcome

Both date columns successfully converted.

---

## Step 11: Validate Order Year

### Code

```python
sales_2020['orderdate'].dt.year.unique()
```

### Result

```python
array([2020])
```

### Finding

All transactions belong to the year 2020.

---

## Step 12: Validate Transaction Date Range

### Code

```python
sales_2020['orderdate'].min()

sales_2020['orderdate'].max()
```

### Purpose

Identify earliest and latest transaction dates.

### Outcome

Confirmed expected sales period for 2020.

---

## Step 13: Validate Key Columns

### Code

```python
sales_2020[
    ['productkey',
     'customerkey',
     'territorykey']
].describe()
```

### Purpose

Review key ranges and identify abnormal values.

### Outcome

Key columns appeared valid.

---

## Step 14: Create Reusable Standardization Function

### Code

```python
def standardize_sales_data(df):

    df.columns = df.columns.str.lower()

    df['orderdate'] = pd.to_datetime(
        df['orderdate']
    )

    df['stockdate'] = pd.to_datetime(
        df['stockdate']
    )

    return df
```

### Purpose

Create a reusable transformation routine for all yearly sales datasets.

### Benefit

Ensures standardized processing for:
- Sales 2020
- Sales 2021
- Sales 2022

---

## Step 15: Apply Standardization Function

### Code

```python
sales_2020 = standardize_sales_data(
    sales_2020
)
```

### Outcome

Successfully applied reusable ETL transformations to the dataset.

---

## Conclusion

AdventureWorks Sales Data 2020 was successfully profiled, validated, and standardized.

Dataset Status: Ready for consolidation with 2021 and 2022 sales datasets.
