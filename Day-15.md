# Day 15

## Pandas
[Open in Google Colab](https://colab.research.google.com/drive/11b9mf_4bVFFFz7PGyP5g2cAMeDrppaOe)

## Overview

Today I learned about **Pandas**, a powerful Python library used for data manipulation, cleaning, and analysis. It helps us work with structured data in the form of rows and columns. Pandas makes it easier to organize, filter, modify, and analyze datasets.

## Topics Covered

### 1. Introduction to Pandas

I learned about Pandas and its importance in data analysis. It provides two main data structures:

- **Series:** A one-dimensional labeled array.
- **DataFrame:** A two-dimensional table containing rows and columns.

**Example:**

```python
import pandas as pd
import numpy as np
```

### 2. Creating a Series

I learned how to create a Pandas Series using a list and assign custom labels as its index.

**Example:**

```python
data = [10, 20, 30, 40, 50]

s = pd.Series(data)
print(s)
```

### 3. Creating a DataFrame

I practiced creating DataFrames using dictionaries and NumPy arrays. A DataFrame stores data in tabular form.

**Example:**

```python
data = {
    'Name': ['Aman', 'Riya', 'Simran'],
    'Age': [20, 21, 19],
    'Marks': [85, 90, 88]
}

df = pd.DataFrame(data)
print(df)
```

### 4. Selecting Rows and Columns

I learned how to access specific rows and columns using `loc` and `iloc`.

- `loc[]` – selects data using labels.
- `iloc[]` – selects data using integer positions.

**Example:**

```python
print(df.loc[0])
print(df.iloc[1])
print(df['Name'])
```

### 5. Adding and Deleting Columns

I practiced adding new columns to a DataFrame and deleting existing columns using `drop()`.

**Example:**

```python
df['City'] = ['Delhi', 'Mumbai', 'Ludhiana']

df = df.drop('Age', axis=1)

print(df)
```

### 6. Conditional Filtering

I learned how to filter rows based on specific conditions.

**Example:**

```python
result = df[df['Marks'] > 85]
print(result)
```

This displays only the rows where marks are greater than 85.

### 7. Setting and Resetting Index

I learned how to set a particular column as the index of a DataFrame and restore the default index using `reset_index()`.

**Example:**

```python
df = df.set_index('Name')
print(df)

df = df.reset_index()
print(df)
```

### 8. Handling Missing Values

I learned how to identify and handle missing values in a dataset.

Some useful functions are:

- `isnull()` – identifies missing values.
- `dropna()` – removes rows or columns containing missing values.
- `fillna()` – replaces missing values with a specified value.

**Example:**

```python
df.isnull()
df.dropna()
df.fillna(0)
```

### 9. Grouping and Aggregation

I learned how to group data based on a particular column and perform calculations using aggregation functions.

**Example:**

```python
data = {
    'Department': ['IT', 'HR', 'IT', 'HR'],
    'Salary': [30000, 25000, 40000, 35000]
}

df = pd.DataFrame(data)

print(df.groupby('Department')['Salary'].mean())
```

### 10. Applying Custom Functions

I learned how to use the `apply()` function to apply a custom function to rows or columns of a DataFrame or to elements of a Series.

**Example:**

```python
def add_bonus(x):
    return x + 1000

df['Updated Salary'] = df['Salary'].apply(add_bonus)
print(df)
```

### 11. Combining DataFrames

I learned how to combine multiple DataFrames using the `concat()` function.

**Example:**

```python
df1 = pd.DataFrame({'Name': ['Aman', 'Riya']})
df2 = pd.DataFrame({'Name': ['Simran', 'Raj']})

result = pd.concat([df1, df2])
print(result)
```

### 12. Reading CSV Files

I learned how to load data from CSV files using the `read_csv()` function.

**Example:**

```python
df = pd.read_csv('data.csv')
print(df)
```

This helps us import external datasets into Python for analysis.

### 13. Exploring a Dataset

I practiced different functions to understand the structure and information of a dataset.

- `head()` – displays the first five rows.
- `tail()` – displays the last five rows.
- `sample()` – displays random rows.
- `columns` – shows column names.
- `shape` – returns the number of rows and columns.
- `info()` – provides information about columns and data types.
- `describe()` – displays statistical summaries of numerical columns.

**Example:**

```python
print(df.head())
print(df.tail())
print(df.shape)
print(df.info())
print(df.describe())
```

## Key Learnings

- Pandas is useful for data manipulation and analysis.
- Series and DataFrame are the two main Pandas data structures.
- `loc` and `iloc` help in selecting specific rows and columns.
- DataFrames can be modified by adding or deleting columns.
- Conditional filtering helps extract required data.
- Missing values can be identified, removed, or replaced.
- `groupby()` and aggregation functions help summarize data.
- `apply()` allows custom functions to be applied to data.
- `concat()` is used to combine multiple DataFrames.
- `read_csv()` helps load external datasets.
- Dataset exploration functions help understand data before analysis.

## Practice Questions

1. Create a Pandas Series using a list of 10 numbers.
2. Create a DataFrame containing student names, ages, and marks.
3. Display the first five and last five rows of a DataFrame.
4. Select a particular column using `loc` and `iloc`.
5. Add a new column to a DataFrame and delete an existing column.
6. Filter students whose marks are greater than 80.
7. Set a column as the index and then reset the index.
8. Create a DataFrame with missing values and handle them using `dropna()` and `fillna()`.
9. Group employee data by department and calculate the average salary.
10. Use `apply()` to increase every student's marks by 5.
11. Combine two DataFrames using `concat()`.
12. Load a CSV file and explore it using `head()`, `info()`, and `describe()`.
