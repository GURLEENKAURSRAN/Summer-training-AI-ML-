# Day-12 Daily Diary – Advanced Functions in Python

[Open Google Colab Notebook](https://colab.research.google.com/drive/16t5U6Lu7V-PHg6BP94febf0PcAqvEm4-?usp=sharing).

## Topic Covered

Today I learned the remaining concepts of **Functions in Python**, including **Types of Functions, Lambda Functions, Recursive Functions, Anonymous Functions, Variable Scope, and Higher-Order Functions**. 

# Types of Functions

Python provides two main types of functions.

## 1. Built-in Functions

Built-in functions are predefined functions provided by Python.

### Examples

```python
print("Hello")
len("Python")
sum([10, 20, 30])
max([5, 8, 2])
```

Some commonly used built-in functions are:

* `print()`
* `len()`
* `sum()`
* `max()`
* `min()`
* `type()`
* `range()`
* `input()`

---

## 2. User-Defined Functions

These are functions created by the programmer using the `def` keyword.

### Example

```python
def greet(name):
    print("Hello", name)

greet("Gurleen")
```

User-defined functions help solve custom problems while improving code readability and reusability.

# Lambda (Anonymous) Functions

A **Lambda Function** is a small anonymous function that can have any number of arguments but only one expression.

### Syntax

```python
lambda arguments: expression
```

### Example

```python
square = lambda x: x * x
print(square(5))
```

**Output**

```
25
```

### Advantages

* Short and concise code.
* Useful for one-line functions.
* Commonly used with `map()`, `filter()`, and `sorted()`.

# Higher-Order Functions

A **Higher-Order Function** is a function that either:

* Takes another function as an argument, or
* Returns a function.

### Common Higher-Order Functions

### `map()`

Applies a function to every element.

```python
numbers = [1, 2, 3, 4]

squares = list(map(lambda x: x*x, numbers))
```

#  Recursive Functions

A **Recursive Function** is a function that calls itself until a base condition is reached.

### Example

```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n-1)

print(factorial(5))
```

**Output**

```
120
```

### Important Points

* Every recursive function must have a **base case**.
* Without a base case, recursion continues indefinitely and causes a recursion error.

#  Variable Scope (Revision)

### Local Variable

A variable declared inside a function.

```python
def demo():
    x = 10
    print(x)
```

---

### Global Variable

A variable declared outside all functions.

```python
x = 100

def demo():
    print(x)
```

---

#  Programs Practiced

* Square using Lambda Function
* Addition using Lambda
* Sorting using `sorted()`
* Filtering even numbers using `filter()`
* Squaring numbers using `map()`
* Recursive factorial
* Recursive Fibonacci series
* Recursive sum of numbers
* Global and local variable examples
* User-defined function programs

---

# 🎯 Key Learnings

* Python provides both built-in and user-defined functions.
* Lambda functions simplify small one-line operations.
* Anonymous functions are created using the `lambda` keyword.
* Higher-order functions work with other functions to make code more efficient.
* Recursive functions solve problems by calling themselves.
* Every recursive function requires a base condition.
* Understanding variable scope helps avoid unexpected behavior in programs.
