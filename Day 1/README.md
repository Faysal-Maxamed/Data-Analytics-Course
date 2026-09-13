# Day 1 – Introduction to Pandas and Dataset Exploration

## Overview

This notebook is the first part of a Python Data Analysis learning series. It introduces the basics of Pandas and demonstrates how to load, inspect, and understand a dataset using Python.

The main focus of this notebook is dataset exploration before data cleaning or deeper analysis.

## Objectives

By completing this notebook, you will learn how to:

* Import the Pandas library
* Load an Excel dataset into Python
* Display the first rows of a dataset
* Display the last rows of a dataset
* Show random samples from a dataset
* Check dataset shape
* Display column names
* Check data types
* View dataset information
* Generate descriptive statistics

## Technologies Used

* Python
* Pandas
* Microsoft Excel (`.xlsx`)

## Dataset

The notebook uses the dataset file below:

* `Customer Demographic Data Analysis Data.xlsx`

This file is located inside the `Day 1` folder and is loaded with `pd.read_excel()`.

## Import Pandas

The notebook starts by importing the Pandas library:

```python
import pandas as pd
```

## Loading the Dataset

```python
data = pd.read_excel("Customer Demographic Data Analysis Data.xlsx")
```

After loading, the dataset can be explored using Pandas functions.

## Dataset Exploration

### 1. Display the First Rows

```python
data.head()
```

This helps quickly view the beginning of the dataset.

### 2. Display the Last Rows

```python
data.tail()
```

This helps inspect the end of the dataset.

### 3. Display Random Rows

```python
data.sample(5)
```

This allows a quick random check of rows.

### 4. Check Dataset Shape

```python
data.shape
```

The notebook shows that the dataset contains:

* 300 rows
* 9 columns

### 5. Display Column Names

```python
data.columns
```

### 6. Check Data Types

```python
data.dtypes
```

### 7. Dataset Information

```python
data.info()
```

### 8. Descriptive Statistics

```python
data.describe(include="all")
```

## Key Pandas Functions Used

| Function / Property | Purpose |
| --- | --- |
| `pd.read_excel()` | Load an Excel file |
| `head()` | Show the first rows |
| `tail()` | Show the last rows |
| `sample()` | Show random rows |
| `shape` | Show number of rows and columns |
| `columns` | Show column names |
| `dtypes` | Show column data types |
| `info()` | Show dataset overview |
| `describe()` | Show descriptive statistics |

## Learning Workflow

The notebook follows this basic flow:

```text
Load Dataset
    ↓
View Data
    ↓
Check Shape
    ↓
Check Columns
    ↓
Check Data Types
    ↓
Check Dataset Information
    ↓
Generate Descriptive Statistics
```

## Why Dataset Exploration Is Important

Before cleaning or analyzing data, it is important to understand:

* How large the dataset is
* What columns are available
* What types of values are present
* Whether missing values exist
* Whether numerical columns have useful statistics

## Project Files

* `Day1.ipynb` – Notebook with Day 1 exercises
* `Customer Demographic Data Analysis Data.xlsx` – Dataset used in the notebook
* `README.md` – Project explanation

## Conclusion

Day 1 focuses on the foundations of dataset exploration using Pandas. These basic skills are important before moving into cleaning, filtering, transformation, and deeper analysis.


---

*Day 1 – Pandas Dataset Exploration*
