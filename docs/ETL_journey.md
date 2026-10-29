# ETL Journey

## Dataset

AdventureWorks Sales Data 2020

---

## Step 1: Import Libraries

```python
import pandas as pd
import numpy as np
```

### Learning

- Pandas is used for data manipulation.
- NumPy is used for numerical operations.

---

## Step 2: Load CSV File

```python
sales_2020 = pd.read_csv(
    "../Data/Raw/AdventureWorks Sales Data 2020.csv"
)
```

### Learning

- Used `pd.read_csv()` to load the dataset.
- Learned that the notebook was running from the Python folder.
- Used relative paths to access files.

---

## Step 3: Verify Current Working Directory

```python
import os
os.getcwd()
```

### Learning

- Notebook was executing from the Python directory.
- Had to move one folder up using `..`.

---

## Step 4: Preview Dataset

```python
sales_2020.head()
```

### Learning

- Verified successful file load.
- Viewed first 5 records.

---

## Step 5: Check Dataset Size

```python
sales_2020.shape
```

### Result

```python
(2630, 8)
```

### Learning

Dataset contains:

- 2630 rows
- 8 columns

---

## Step 6: Review Column Names

```python
sales_2020.columns
```

### Learning

Identified the following columns:

- OrderDate
- StockDate
- OrderNumber
- ProductKey
- CustomerKey
- TerritoryKey
- OrderLineItem
- OrderQuantity

---

## Step 7: Standardize Column Names

```python
sales_2020.columns = sales_2020.columns.str.lower()
```

### Learning

Converted all column names to lowercase to make coding easier and maintain consistency.

---

## Step 8: Check Data Types

```python
sales_2020.dtypes
```

### Learning

Observed:
- Date columns loaded as strings
- Numeric columns loaded as integers

---

## Step 9: Check Missing Values

```python
sales_2020.isnull().sum()
```

### Learning

Verified completeness of the data.

---

## Step 10: Check Duplicate Records

```python
sales_2020.duplicated().sum()
```

### Result

```python
0
```

### Learning

No duplicate records found.

---

## Step 11: Convert Date Columns

```python
sales_2020['orderdate'] = pd.to_datetime(
    sales_2020['orderdate']
)

sales_2020['stockdate'] = pd.to_datetime(
    sales_2020['stockdate']
)
```

### Learning

Converted string dates into datetime format.

---

## Step 12: Validate Order Year

```python
sales_2020['orderdate'].dt.year.unique()
```

### Result

```python
array([2020])
```

### Learning

All transactions belong to the year 2020.
