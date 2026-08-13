# Day 14 - 08 August 2026

## NumPy
[Open in Google Colab](https://colab.research.google.com/drive/1AOXIokkan36w15IH22vdwFlLCTtCHRrX?usp=sharing)

## Overview

Today I learned about **NumPy (Numerical Python)**, a powerful Python library used for numerical computations and working with arrays and matrices. NumPy provides efficient ways to store, manipulate, and perform mathematical operations on large amounts of numerical data.

## Topics Covered

### 1. Creating NumPy Arrays

I learned how to create NumPy arrays using `np.array()`.

**Example:**

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

NumPy arrays can be one-dimensional or multi-dimensional. I also learned how to check the shape of an array using `.shape`.

### 2. Creating Arrays Using NumPy Functions

I practiced creating arrays using different NumPy functions such as:

* `np.zeros()` – creates an array filled with zeros
* `np.ones()` – creates an array filled with ones
* `np.full()` – creates an array filled with a specific value
* `np.arange()` – generates a sequence of numbers
* `np.identity()` – creates an identity matrix

**Example:**

```python
arr = np.arange(1, 21)
print(arr)
```

### 3. Reshaping Arrays

I learned how to change the shape of an array using the `reshape()` function without changing its elements.

**Example:**

```python
arr = np.arange(12)

matrix = arr.reshape(3, 4)
print(matrix)
```

This converts a 1D array containing 12 elements into a `3 × 4` matrix.

### 4. Indexing and Slicing

I learned how to access individual elements and specific parts of NumPy arrays using indexing and slicing.

**Example:**

```python
arr = np.array([10, 20, 30, 40, 50])

print(arr[2])
print(arr[1:4])
```

For 2D arrays, slicing can also be used to extract specific rows or columns.

### 5. Sorting Arrays

I practiced sorting elements of a NumPy array.

**Example:**

```python
arr = np.array([23, 10, 25, 45, 5])

arr.sort()
print(arr)
```

Difference between Python's `sorted()` function and NumPy's `.sort()` method.

### 6. Slicing and Copying

I learned that slicing a NumPy array can create a view of the original array, meaning changes made to the sliced array can also affect the original array.

To create an independent copy, I used the `copy()` method.

**Example:**

```python
arr = np.array([10, 20, 30, 40, 50])

new_arr = arr.copy()
new_arr[0] = 100

print(arr)
print(new_arr)
```

### 7. Broadcasting

I learned about **broadcasting**, which allows NumPy to perform operations on arrays without manually repeating values.

**Example:**

```python
arr = np.array([1, 2, 3, 4])

print(arr * 10)
```

The value `10` is automatically applied to every element of the array.

### 8. Conditional Operations

I learned how to apply conditions to NumPy arrays and filter elements based on those conditions.

**Example:**

```python
arr = np.array([10, 15, 20, 25, 30])

print(arr[arr % 2 == 0])
```

This extracts the even numbers from the array.

### 9. Aggregate Functions

I practiced different aggregate functions to perform calculations on arrays.

* `min()` – finds the minimum value
* `max()` – finds the maximum value
* `sum()` – calculates the sum
* `argmin()` – returns the index of the minimum value
* `argmax()` – returns the index of the maximum value

**Example:**

```python
arr = np.array([10, 20, 5, 40, 15])

print(arr.min())
print(arr.max())
print(arr.sum())
```

### 10. Mathematical Functions

I learned how NumPy provides built-in mathematical functions for performing calculations on array elements.

**Example:**

```python
arr = np.array([1, 4, 9, 16])

print(np.sqrt(arr))
```

I also practiced functions such as `np.sin()` for performing mathematical operations on arrays.

### 11. Identity Matrix

I learned how to generate an identity matrix using `np.identity()`.

**Example:**

```python
matrix = np.identity(4, dtype=int)
print(matrix)
```

This creates a `4 × 4` matrix with `1` on the main diagonal and `0` elsewhere.

### 12. Random Number Generation

I learned how to generate random integers using NumPy.

**Example:**

```python
random_numbers = np.random.randint(1, 100, size=5)
print(random_numbers)
```

This generates 5 random integers within the specified range.

### 13. Linspace

I also learned about `np.linspace()`, which generates evenly spaced numbers between a starting and ending value.

**Example:**

```python
arr = np.linspace(10, 100, 10)
print(arr)
```

## Key Learnings

* NumPy is mainly used for numerical computations and working with arrays.
* `np.array()` is used to create NumPy arrays.
* `np.arange()` can be used to generate a sequence of numbers.
* `reshape()` changes the dimensions of an array.
* Indexing and slicing help access specific elements and parts of arrays.
* NumPy provides useful mathematical and aggregate functions.
* Broadcasting allows operations to be performed efficiently on arrays.
* `copy()` creates an independent copy of an array.
* NumPy can generate random numbers and identity matrices.
* NumPy is useful for data analysis, scientific computing, and machine learning.


## Practice Questions

1. Create a NumPy array containing numbers from 1 to 20.

2. Generate a `3 × 3` NumPy array filled with zeros.

3. Create a `5 × 5` matrix containing values from 1 to 25 and extract its diagonal elements.

4. Create a 1D NumPy array containing even numbers between 10 and 30.

5. Create an array containing 12 elements and reshape it into a `3 × 4` matrix.

6. Find the maximum, minimum, and mean values of a NumPy array.

7. Perform element-wise addition, subtraction, and multiplication on two NumPy arrays.

8. Create a 2D NumPy array and extract its second row using slicing.

9. Generate an identity matrix of size `4 × 4`.

10. Use NumPy to generate 5 random integers between 1 and 100.

11. Find the square root and standard deviation of the elements in a NumPy array.
