# task19
# Task 19 -- Duplicate Records and Data Validation

## Objective

Identify duplicate records and perform basic data validation checks
using Pandas.

## Tools Used

-   Python
-   Pandas
-   Jupyter Notebook

## Dataset

Columns: - ID - Name - Age - Salary

## Programs

### 1. Import Pandas

``` python
import pandas as pd
```

### 2. Create DataFrame

``` python
import pandas as pd
data = {
    "ID":[101,102,103,104,104,105],
    "Name":["John","Alice","Bob","David","David","Eva"],
    "Age":[25,30,22,29,29,35],
    "Salary":[50000,60000,45000,70000,70000,80000]
}
df = pd.DataFrame(data)
print(df)
```

### 3. Find Duplicate Rows

``` python
duplicates = df.duplicated()
print(duplicates)
```

### 4. Display Duplicate Rows

``` python
duplicate_rows = df[df.duplicated()]
print(duplicate_rows)
```

### 5. Remove Duplicate Rows

``` python
clean_df = df.drop_duplicates()
print(clean_df)
```

## Data Validation Checks

``` python
print(df.isnull())
print(df.isnull().sum())
valid_age = df[(df["Age"]>=18) & (df["Age"]<=60)]
valid_salary = df[df["Salary"]>0]
duplicate_id = df[df["ID"].duplicated()]
print(df["Name"].unique())
print(df["Name"].nunique())
print(df.dtypes)
print(df.describe())
print(df.columns)
```

## Concepts Learned

-   Detect duplicate records
-   Remove duplicates
-   Check missing values
-   Validate data ranges
-   Validate IDs
-   Check unique values
-   Verify data types
-   Generate summary statistics

## Deliverables

-   Duplicate record analysis
-   Cleaned dataset
-   Five or more data validation checks completed

## Outcome

Successfully cleaned duplicate records and validated dataset quality
using Pandas.

**Intern:** Jasmitha\
**Organization:** Veda Technology
