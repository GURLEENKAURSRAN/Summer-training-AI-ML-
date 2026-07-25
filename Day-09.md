#  Day-9 Daily Diary – `for` Loop in Python

[Open Google Colab Noteboo](https://colab.research.google.com/drive/1cq2c1Vqi62yQiAlqXfDx96AxGrgJUCvY?usp=sharing)

What are Loops?

A loop is a programming construct that repeatedly executes a block of code until a specified condition is met or until all elements in a sequence have been processed.

Why use loops?
Avoid writing repetitive code.
Process collections such as lists, strings, tuples, and dictionaries.
Perform repetitive calculations.
Automate tasks that require multiple iterations.

# What is a `for` Loop?

A **`for` loop** is a control flow statement that repeats a block of code for each item in a sequence. It is commonly used when the number of iterations is known or when traversing collections.

### Syntax

```python
for variable in sequence:
    # code to execute
```

---

#  `range()` Function

The `range()` function generates a sequence of numbers and is most commonly used with `for` loops.

### Forms of `range()`

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

### Example

```python
for i in range(1, 6):
    print(i)
```

**Output**

```
1
2
3
4
5
```

### Key Points

* The **start** value is included.
* The **stop** value is excluded.
* The default start value is `0`.
* The default step size is `1`.

# Iterating Through Different Data Types

### 1. Looping Through a List

```python
fruits = ["Apple", "Mango", "Orange"]

for fruit in fruits:
    print(fruit)
```

### 2. Looping Through a String

```python
name = "Python"

for ch in name:
    print(ch)
```

### 3. Looping Through a Tuple

```python
days = ("Mon", "Tue", "Wed")

for day in days:
    print(day)
```

### 4. Looping Through a Dictionary

```python
student = {"Name": "John", "Marks": 90}

for key, value in student.items():
    print(key, value)
```

# Programs Practiced

* Print numbers from 1 to 10.
* Print squares of numbers.
* Print even numbers.
* Print odd numbers.
* Calculate the sum of numbers.
* Find the factorial of a number.
* Generate the Fibonacci series.
* Check whether a number is prime.
* Count vowels in a string.
* Reverse a list.
* Find the largest number in a list.
* Count occurrences of an element.
* Create a list of squared numbers.
* Print multiplication tables.
* Traverse lists, strings, tuples, dictionaries, and sets.
* Print star patterns using nested `for` loops.

# Key Learnings

* A `for` loop repeats code efficiently without duplication.
* `range()` is commonly used to generate sequences of numbers.
* A `for` loop can iterate through lists, strings, tuples, dictionaries, and sets.
* Nested `for` loops are useful for pattern printing and multiplication tables.
* Proper indentation is essential for correct loop execution.

The `for` loop is one of the most commonly used loops in Python. It makes repetitive tasks simple, readable, and efficient, making it an essential concept for solving programming problems and working with collections of data.

