# Day 16

## Matplotlib
[Open in Google Colab](https://colab.research.google.com/drive/11b9mf_4bVFFFz7PGyP5g2cAMeDrppaOe)

## Overview

Today I learned about **Matplotlib**, a popular Python library used for creating data visualizations such as graphs, charts, and plots. It helps represent data in a visual and easy-to-understand way, making it useful for data analysis and presentations.

## Topics Covered

### 1. Introduction to Matplotlib

I learned about the Matplotlib library and its `pyplot` module, which is commonly used to create different types of graphs.

**Example:**

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array([1, 2])
y = np.array([2, 3])

plt.plot(x, y)
plt.show()
```

### 2. Creating Line Plots

I learned how to create basic line plots using the `plot()` function to represent relationships between values.

**Example:**

```python
x = np.array([1, 2, 3, 4])
y = np.array([2, 4, 6, 8])

plt.plot(x, y)
plt.show()
```

I also practiced plotting data from a CSV file using Pandas.

### 3. Markers in Plots

I learned how to use markers to highlight individual data points on a graph.

Some commonly used markers include:

- `'*'` – Star marker
- `'+'` – Plus marker
- `'o'` – Circle marker
- `'s'` – Square marker

**Example:**

```python
x = np.array([1, 2, 3])
y = np.array([2, 4, 6])

plt.plot(x, y, marker='*')
plt.show()
```

### 4. Line Styles and Colors

I practiced changing the appearance of lines using different styles and colors.

Common line styles:

- `solid` – Solid line
- `dotted` – Dotted line
- `dashed` – Dashed line
- `dashdot` – Dash-dot line

**Example:**

```python
plt.plot(x, y, marker='*', 
         linestyle='dotted', color='green')
plt.show()
```

### 5. Customizing Markers and Line Width

I learned how to customize markers and lines using different properties:

- `linewidth` – Changes line thickness.
- `ms` – Changes marker size.
- `mec` – Sets marker edge color.
- `mfc` – Sets marker face color.

**Example:**

```python
plt.plot(x, y, marker='*', color='blue',
         ms=15, mec='red', mfc='green',
         linewidth=3)

plt.show()
```

### 6. Adding Titles and Labels

I learned how to add titles and axis labels to make graphs more informative. I also practiced changing font family, size, and color using `fontdict`.

**Example:**

```python
plt.title("Sports Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burn")

plt.plot(x, y)
plt.show()
```

### 7. Subplots

I learned how to display multiple plots in a single figure using the `subplot()` function.

The syntax is:

`plt.subplot(rows, columns, position)`

**Example:**

```python
plt.subplot(2, 2, 1)
plt.plot([1, 2, 3], [2, 4, 6])

plt.subplot(2, 2, 2)
plt.plot([1, 2, 3], [6, 4, 2])

plt.subplot(2, 2, 3)
plt.plot([1, 2, 3], [1, 3, 5])

plt.subplot(2, 2, 4)
plt.plot([1, 2, 3], [5, 3, 1])

plt.show()
```

### 8. Figure and Axes

I learned how to create figures and add multiple axes using `figure()` and `add_axes()`.

**Example:**

```python
fig = plt.figure()

axes1 = fig.add_axes([0.1, 0.2, 0.9, 0.9])
axes1.plot([1, 2, 3], [2, 4, 6], 'r')

axes2 = fig.add_axes([0.15, 0.75, 0.3, 0.3])
axes2.plot([1, 2, 3], [6, 4, 2], 'b')

plt.show()
```

### 9. Pie Charts

I learned how to create pie charts using the `pie()` function to represent data in proportions or percentages.

I also practiced using `labels`, `explode`, and `autopct` to customize pie charts.

**Example:**

```python
sizes = [234, 567, 223, 123]
labels = ['Python', 'C++', 'Java', 'Excel']

plt.pie(sizes, labels=labels, autopct='%1.2f%%')
plt.show()
```

### 10. Bar Graphs

I learned how to create vertical bar graphs using the `bar()` function to compare different categories of data.

**Example:**

```python
x = [1, 2, 3, 4]
y = [20, 40, 30, 60]

plt.bar(x, y)
plt.title("Bar Graph")
plt.xlabel("Categories")
plt.ylabel("Values")

plt.show()
```

### 11. Horizontal Bar Graphs

I practiced creating horizontal bar graphs using the `barh()` function.

**Example:**

```python
x = [1, 2, 3, 4]
y = [20, 40, 30, 60]

plt.barh(x, y)
plt.title("Horizontal Bar Graph")
plt.show()
```

### 12. Histograms

I learned how to create histograms using the `hist()` function. Histograms help represent the frequency distribution of numerical data.

**Example:**

```python
data = np.array([33, 55, 66, 23, 45, 67, 87])

plt.hist(data)
plt.title("Histogram")
plt.show()
```

### 13. Box Plots

I learned how to create box plots using the `boxplot()` function. Box plots help visualize the distribution of data and identify possible outliers.

**Example:**

```python
data = [np.random.normal(0, std, 99) 
        for std in range(1, 7)]

plt.boxplot(data)
plt.show()
```

### 14. Taking User Input

I also practiced taking input from users and converting comma-separated values into a tuple using `input()` and `split()`.

**Example:**

```python
user_input = input("Enter values separated by commas: ")

t = tuple(user_input.split(','))
print(t)
```

## Key Learnings

- Matplotlib is useful for creating data visualizations in Python.
- `pyplot` provides functions for creating and customizing graphs.
- `plot()` is used to create line plots.
- Markers, line styles, and colors help customize graphs.
- Titles and axis labels make visualizations easier to understand.
- `subplot()` allows multiple plots in one figure.
- `figure()` and `add_axes()` help create and manage plotting areas.
- Pie charts represent proportions of data.
- Bar graphs help compare different categories.
- Histograms show frequency distributions.
- Box plots help understand data distribution and identify possible outliers.

## Practice Questions

1. Create a simple line plot using two NumPy arrays.
2. Create a line plot using different markers and line styles.
3. Change the color, marker size, and linewidth of a graph.
4. Add a title, X-axis label, and Y-axis label to a plot.
5. Create four different plots using `subplot()`.
6. Create a figure with two axes using `figure()` and `add_axes()`.
7. Create a pie chart for five programming languages and display percentages.
8. Create a vertical bar graph to compare marks of five students.
9. Create a horizontal bar graph using `barh()`.
10. Generate a NumPy array and create a histogram using `hist()`.
11. Generate random data using `np.random.normal()` and display it using a box plot.
12. Take comma-separated values from the user and convert them into a tuple.
