# Day 18 – Exploratory Data Analysis (EDA)

[Google Colab Link](https://colab.research.google.com/drive/10maKQ80nmr_AevX6FP1feCEUBPIWVhmp)

## Topics Covered

### 1. What is EDA?

EDA stands for **Exploratory Data Analysis**.

It is the process of understanding and analyzing a dataset to discover patterns, identify missing values and outliers, and understand relationships between different columns.

**Uses of EDA:**
- Detect missing values and duplicate rows.
- Identify outliers.
- Understand data distribution.
- Check relationships between features.
- Analyze categorical data.
- Help in feature selection.
- Support better preprocessing and model selection.
- Generate useful insights from data.

### 2. Steps of EDA

The main steps of EDA are:

1. Collect Data
2. Understand Data
3. Clean Data
4. Analyze Data
5. Visualize Data
6. Prepare Data for Machine Learning

### 3. Importing Required Libraries

I imported NumPy, Pandas, Matplotlib, and Seaborn for data analysis and visualization.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

### 4. Reading the Dataset

I used the Titanic dataset for performing EDA.

```python
df = pd.read_csv("/content/Titanic-Dataset.csv")
```

The `read_csv()` function is used to read CSV files and store the data in a Pandas DataFrame.

### 5. Understanding the Dataset

I used different Pandas functions to explore the dataset.

**Displaying the first five rows:**

```python
df.head()
```

**Displaying the last five rows:**

```python
df.tail()
```

**Displaying a random row:**

```python
df.sample()
```

**Getting statistical information:**

```python
df.describe()
```

**Getting dataset information:**

```python
df.info()
```

The `info()` function provides information about column names, data types, non-null values, and memory usage.

### 6. Data Visualization

Data visualization helps us understand patterns and relationships through graphs.

I used Seaborn's `jointplot()` to analyze the relationship between Age and Fare based on gender.

```python
sns.jointplot(
    x='Age',
    y='Fare',
    hue='Sex',
    data=df
)

plt.show()
```

### 7. Data Cleaning

Data cleaning is the process of identifying and handling missing or incorrect values to improve data quality.

**Checking missing values:**

```python
df.isnull()
```

This function returns True for missing values and False for non-missing values.

```python
df.isnull().sum()
```

This gives the number of missing values in each column.

### 8. Encoding Categorical Data

Encoding is the process of converting categorical data into numerical form so that machine learning algorithms can process it.

**Label Encoding:**
- Assigns numerical labels to different categories.
- Useful for converting categorical values into numbers.

**One-Hot Encoding:**
- Creates separate binary columns for categories.
- Useful for nominal categorical features with a small number of unique values.

**Cardinality:** Cardinality refers to the number of unique values in a column.

- **Low Cardinality:** A column has a small number of unique values, such as Sex (male, female).
- **High Cardinality:** A column has many unique values, such as Name, Ticket, and Cabin.

### 9. Finding Outliers

Outliers are data points that are significantly different from other values in a dataset.

I used Seaborn's boxplot to identify outliers in different columns.

```python
sns.boxplot(x='Sex', y='Age', data=df)
plt.show()
```

```python
sns.boxplot(x='Pclass', y='Fare', data=df)
plt.show()
```

I also used a boxplot to visualize numerical columns together.

```python
sns.boxplot(data=df)
plt.show()
```

### 10. Handling Outliers

I learned about the Winsorization technique for handling outliers.

Winsorization limits extreme values by replacing them with specified percentile values.

```python
from scipy.stats.mstats import winsorize

df['Fare'] = winsorize(df['Fare'], limits=[0.05, 0.05])
```

Here, the lower 5% and upper 5% of values are limited to their respective percentile boundaries.

### 11. Data Distribution Using Histogram

A histogram is used to understand the distribution and frequency of numerical data.

```python
plt.hist(df['Age'].dropna())

plt.xlabel('Age')
plt.ylabel('Frequency')
plt.title('Distribution of Age')

plt.show()
```

### 12. Pairplot

A pairplot is used to visualize relationships between multiple numerical features in a dataset.

```python
sns.pairplot(df)
plt.show()
```

It helps identify patterns, distributions, and relationships between variables.

### 13. Data Standardization

Standardization is the process of transforming numerical features to a common scale.

I learned about two commonly used scaling techniques:

**StandardScaler:**

- Transforms data to have a mean of 0 and standard deviation of 1.
- Useful for many distance-based algorithms.
- Helps optimization algorithms such as gradient descent.

```python
from sklearn.preprocessing import StandardScaler

ss = StandardScaler()

df[['Fare']] = ss.fit_transform(df[['Fare']])
```

**MinMaxScaler:**

- Scales values within a fixed range, usually 0 to 1.
- Preserves the overall distribution shape.
- Useful when a bounded range is required.

```python
from sklearn.preprocessing import MinMaxScaler

ms = MinMaxScaler()

df[['Fare']] = ms.fit_transform(df[['Fare']])
```

## Key Learnings

1. Understood the meaning and importance of Exploratory Data Analysis.
2. Learned the different steps involved in EDA.
3. Explored the Titanic dataset using Pandas.
4. Learned to inspect data using `head()`, `tail()`, `describe()`, and `info()`.
5. Understood how to identify missing values.
6. Learned about Label Encoding and One-Hot Encoding.
7. Understood low and high cardinality.
8. Learned to identify outliers using boxplots.
9. Explored Winsorization for handling outliers.
10. Learned data visualization using Matplotlib and Seaborn.
11. Understood StandardScaler and MinMaxScaler.

## Practice Questions

1. What is Exploratory Data Analysis (EDA)?
2. Why is EDA important before training a Machine Learning model?
3. What are the main steps of EDA?
4. What is the purpose of `df.describe()`?
5. How can we check missing values in a dataset?
6. What is the difference between Label Encoding and One-Hot Encoding?
7. What is cardinality? Explain low and high cardinality.
8. What are outliers?
9. How can boxplots help in detecting outliers?
10. What is Winsorization?
11. What is the difference between StandardScaler and MinMaxScaler?
12. What is the purpose of a histogram and pairplot?

