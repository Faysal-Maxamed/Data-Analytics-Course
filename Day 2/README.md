# Day 2 – Pandas Data Selection, Filtering & Sorting

## Overview

This notebook introduces the basics of selecting, filtering, and sorting data using Python and Pandas. It uses the customer demographic dataset and focuses on practical DataFrame operations for data analysis.

## Objectives

By completing this notebook, you will learn how to:

- Import the Pandas library
- Load an Excel dataset into Python
- Select a single column
- Select multiple columns
- Use `iloc` to select rows and columns by position
- Use `loc` to select rows and columns by labels
- Filter data using conditions
- Filter records using multiple categories with `isin()`
- Combine multiple conditions using `&`
- Sort data in ascending or descending order

## Technologies Used

- Python
- Pandas
- Microsoft Excel (`.xlsx`)

## Dataset

The notebook uses the file below:

- `Customer Demographic Data Analysis Data.xlsx`

This dataset is loaded with Pandas using:

```python
data2 = pd.read_excel("Customer Demographic Data Analysis Data.xlsx")
```

## Notebook Workflow

### 1. Import Pandas

```python
import pandas as pd
```

### 2. Load the Dataset

```python
data2 = pd.read_excel("Customer Demographic Data Analysis Data.xlsx")
```

### 3. Select a Single Column

```python
data2['Gender']
```

### 4. Select Multiple Columns

```python
data2[['Occupation','City','Monthly_Income']]
```

### 5. Select Rows with `iloc`

```python
data2.iloc[299]
```

```python
data2.iloc[1:10]
```

### 6. Select Rows and Columns with `loc`

```python
data2.loc[10:100, ['Gender', 'Occupation']]
```

### 7. Filter Data

```python
data2[data2['Occupation'] == 'Civil Servant']
```

### 8. Filter Multiple Categories

```python
data2[data2['Gender'].isin(['Female', 'NaN'])]
```

### 9. Apply Multiple Conditions

```python
data2[
    (data2['Gender'] == 'Female') &
    (data2['Occupation'] == 'Civil Servant') &
    (data2['City'] =='Mogadishu')
]
```

### 10. Sort Data

```python
data2.sort_values('Gender', ascending=True)
data2.sort_values('Gender', ascending=False)
```

## Key Pandas Concepts Used

- `pd.read_excel()`
- `data2['Column']`
- `data2[['A', 'B']]`
- `iloc[]`
- `loc[]`
- `isin()`
- Boolean filtering
- `&` for multiple conditions
- `sort_values()`

## Project Files

- `Day2.ipynb` – Notebook with Day 2 exercises
- `Customer Demographic Data Analysis Data.xlsx` – Dataset used in the notebook
- `README.md` – Project explanation

## Author

Faysal Mohamed Daahir

## Conclusion

Day 2 focuses on practical Pandas operations for selecting, filtering, and sorting data. These skills are essential for preparing datasets for analysis and visualization.
