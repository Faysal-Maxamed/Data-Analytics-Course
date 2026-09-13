# Day 3 – Data Cleaning and Data Type Conversion

## Overview

This notebook focuses on data cleaning, standardization, and data type conversion using Python and Pandas. It uses the customer demographic dataset and demonstrates how to inspect the data, clean inconsistent values, rename columns, and convert columns into the correct format for analysis.

## Objectives

By completing this notebook, you will learn how to:

- Import the Pandas library
- Load an Excel dataset into Python
- Display the first rows of a dataset
- View a single column
- Check dataset data types
- Count category values in a column
- Rename columns
- Replace inconsistent values in text columns
- Clean and standardize category labels
- Convert numeric columns into the correct data type

## Technologies Used

- Python
- Pandas
- Microsoft Excel (`.xlsx`)

## Dataset

The notebook uses the file below:

- `Customer Demographic Data Analysis Data.xlsx`

This dataset is loaded with Pandas using:

```python
data = pd.read_excel(
    "Customer Demographic Data Analysis Data.xlsx"
)
```

## Notebook Workflow

### 1. Import Pandas

```python
import pandas as pd
```

### 2. Load the Dataset

```python
data = pd.read_excel(
    "Customer Demographic Data Analysis Data.xlsx"
)
```

### 3. View the First Rows

```python
data.head()
```

### 4. Select a Column

```python
data['Gender']
```

### 5. Check Data Types

```python
data.dtypes
```

### 6. View Value Counts

```python
data['Occupation'].value_counts()
```

### 7. Rename a Column

```python
data.rename(columns={"Customer_ID": "CUD"})
```

### 8. Standardize Occupation Values

```python
data['Occupation'] = data['Occupation'].replace("CS", "CIVIL SERVANT")
```

### 9. Clean Gender Values

```python
data['Gender'] = data['Gender'].replace("MALE", "Male")
data['Gender'] = data['Gender'].replace("male", "Male")
data['Gender'] = data['Gender'].replace("female", "Female")
```

### 10. Clean City Values

```python
data['City'] = data['City'].replace("Mogadishu", "Mog")
```

### 11. Check Data Types Again

```python
data.dtypes
```

### 12. Convert Age to Float

```python
data['Age'] = data['Age'].astype(float)
```

### 13. Convert Monthly Income to Numeric

```python
data['Monthly_Income'] = pd.to_numeric(
    data['Monthly_Income'],
    errors="coerce"
)
```

## Key Pandas Concepts Used

- `pd.read_excel()`
- `head()`
- `value_counts()`
- `rename(columns=...)`
- `replace()`
- `astype()`
- `pd.to_numeric()`
- `errors="coerce"`

## Data Cleaning Focus

This notebook mainly focuses on cleaning inconsistent text values and preparing the dataset for analysis. Examples include:

- Standardizing gender labels
- Replacing inconsistent occupation values
- Cleaning city names
- Converting Age and Monthly_Income into proper numeric formats

## Project Files

- `Day3.ipynb` – Notebook with Day 3 exercises
- `Customer Demographic Data Analysis Data.xlsx` – Dataset used in the notebook
- `README.md` – Project explanation
- `Screenshots/` – Images related to the project

## Author

Faysal Mohamed Daahir

## Conclusion

Day 3 is focused on cleaning and preparing a real dataset for analysis. The notebook shows how important it is to standardize values and convert columns into the correct data types before exploring or visualizing data.
