# Day 03 - Tuples in Python

[Open Google Colab Notebook](https://colab.research.google.com/drive/1wgiQxSft9_1zEQCN_HZqS0OrmxZ5aN32?usp=sharing)

## Introduction

A tuple is an ordered collection of items in Python. Tuples are similar to lists, but they are **immutable**, meaning their elements cannot be changed after creation.

Tuples are created using parentheses `()` and elements are separated by commas `,`.

---

## Creating Tuples

### Empty Tuple

```python
empty_tuple = ()
print(type(empty_tuple))
```

### Tuple with Elements

```python
fruits = ('apple', 'orange', 'banana')
print(fruits)
```

### Single Element Tuple

```python
single_element_tuple = ("42",)
print(type(single_element_tuple))
```

**Output:**

```python
<class 'tuple'>
```

---

## Using the tuple() Constructor

```python
mytuple = tuple(("apple", "banana", "cherry"))
print(mytuple)
print(type(mytuple))
```

**Output:**

```python
('apple', 'banana', 'cherry')
<class 'tuple'>
```

---

## Accessing Elements

Tuple elements can be accessed using indexing.

```python
fruits = ('apple', 'orange', 'banana')
print(fruits[1])
```

**Output:**

```python
orange
```

---

## Check if Item Exists

```python
City = ("DELHI", "MUMBAI", "KOTA", "LUDHIANA")

if "LUDHIANA" in City:
    print("Yes, 'LUDHIANA' is in the city tuple")
else:
    print("No, 'LUDHIANA' is not in city tuple")
```

**Output:**

```python
Yes, 'LUDHIANA' is in the city tuple
```

---

## Immutable Nature of Tuples

Once a tuple is created, its elements cannot be modified.

```python
Countries = ("INDIA", "SRI LANKA", "AMERICA")
Countries[0] = "PAKISTAN"
```

**Output:**

```python
TypeError: 'tuple' object does not support item assignment
```

### Why this error occurs?

Tuples are immutable, meaning their values cannot be changed after creation.

---

## Workaround: Modify a Tuple

Convert the tuple to a list, make changes, and convert it back.

```python
Country = ("INDIA", "SRI LANKA", "AMERICA")

y = list(Country)
y[1] = "BANGLADESH"

x = tuple(y)

print(x)
print(type(x))
```

**Output:**

```python
('INDIA', 'BANGLADESH', 'AMERICA')
<class 'tuple'>
```

---

## count() Method

The `count()` method returns the number of times an element appears in a tuple.

### Syntax

```python
tuple.count(element)
```

### Example

```python
Tuple1 = (0, 1, 2, 3, 2, 3, 1, 3, 2)

res = Tuple1.count(3)

print("Count of 3 in Tuple1 is:", res)
```

**Output:**

```python
Count of 3 in Tuple1 is: 3
```

---

## index() Method

The `index()` method returns the index of the first occurrence of a specified value.

### Syntax

```python
tuple.index(element, start, end)
```

### Example

```python
Tuple = (0, 1, 2, 3, 2, 3, 1, 3, 2)

print(Tuple.index(3))
print(Tuple.index(3, 4, 6))
```

**Output:**

```python
3
5
```

### Error Example

```python
Tuple = (0, 1, 2, 3, 2, 3, 1, 3, 2)

Tuple.index(4)
```

**Output:**

```python
ValueError: tuple.index(x): x not in tuple
```

---

## Tuple Slicing

```python
numbers = (1, 2, 3, 4, 5)

print(numbers[1:4])
```

**Output:**

```python
(2, 3, 4)
```

---

## Reversing a Tuple

```python
numbers = (1, 2, 3, 4, 5)

print(numbers[::-1])
```

**Output:**

```python
(5, 4, 3, 2, 1)
```

---

## Advantages of Tuples

- Immutable (data remains unchanged)
- Faster than lists for some operations
- Can be used as dictionary keys
- Useful for storing fixed data

---

## Practice Questions

1. Create a tuple named `colors` with elements `'red'`, `'green'`, and `'blue'`. Print the second element.

2. Explain why tuples are immutable and try modifying an element.

3. Given:

```python
numbers = (1, 2, 3, 4, 5)
```

Extract elements from index 1 to 3 and reverse the tuple.

4. Create:

```python
fruits = ('apple', 'banana')
berries = ('strawberry', 'blueberry')
```

Concatenate them and repeat the resulting tuple three times.

5. Create:

```python
grades = (90, 85, 92, 88, 95)
```

- Find how many times 88 appears.
- Find the index of 92.

6. Explain one advantage of tuples over lists.

7. Create:

```python
mixed_types = ('apple', 42, 3.14)
```

Print the second element.

8. Convert:

```python
['cat', 'dog', 'rabbit']
```

into a tuple.

9. Create a nested tuple:

```python
outer_tuple = ('apple', ('red', 'green', 'yellow'))
```

Print `'green'`.

---

## Summary

In this lesson, we learned:

- Creating tuples
- Accessing tuple elements
- Checking membership using `in`
- Tuple immutability
- Converting tuples to lists
- `count()` and `index()` methods
- Tuple slicing and reversing
- Advantages of tuples
