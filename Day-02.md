# Day 02 – Python Data Types: Lists

## Google Colab Notebook

[Open Day 02 Notebook]((https://colab.research.google.com/drive/1WEmoLfVV1eby18e-OarqhraPl40v7v1r?usp=sharing))
## Overview

Today I learned about **Lists in Python**, one of the most commonly used data structures for storing multiple values in a single variable. Lists are flexible, dynamic, and allow different types of data to be stored together.

## Topics Covered

### What is a List?

A list is an ordered collection of items enclosed in square brackets `[]`.

**Example:**

```python
my_list = ["apple", "banana", "cherry", 24, 78.9, True]
```

### Characteristics of Lists

* Ordered
* Zero-indexed
* Mutable (can be modified)
* Can store different data types
* Allow duplicate values
* Dynamic in size
* Support nesting (lists inside lists)
* Iterable using loops
* Support slicing and concatenation

### Creating Lists

```python
fruits = ["apple", "banana", "cherry"]

# Using list() constructor
fruits = list(("apple", "banana", "cherry"))
```

### Common List Methods Learned

#### append()

Adds an item to the end of a list.

```python
UNI = ["CTU", "KTU", "DTU"]
UNI.append("CU")
```

#### clear()

Removes all elements from a list.

```python
UNI.clear()
```

#### copy()

Creates a copy of a list.

```python
new_list = UNI.copy()
```

#### count()

Counts the occurrence of an element.

```python
UNI.count("CTU")
```

#### extend()

Combines two lists.

```python
UNI2.extend(UNI)
```

#### index()

Returns the index of the first occurrence.

```python
UNI.index("KTU")
```

#### insert()

Adds an element at a specific position.

```python
UNI.insert(1, "PUNJABI UNIVERSITY")
```

#### pop()

Removes an element by index (default: last element).

```python
FUR.pop()
```

#### remove()

Removes an element by value.

```python
FUR.remove("CHAIR")
```

#### reverse()

Reverses the order of elements.

```python
FUR.reverse()
```

#### sort()

Sorts the list in ascending order.

```python
FUR.sort()
```

---

## List Slicing

I also learned how to extract specific portions of a list using slicing.

### Syntax

```python
list[start:stop:step]
```

### Examples

```python
numbers = [1,2,3,4,5,6,7,8,9]

numbers[2:6]     # [3,4,5,6]
numbers[:4]      # [1,2,3,4]
numbers[5:]      # [6,7,8,9]
numbers[::-1]    # Reverse list
numbers[::2]     # Every second element
```

### Key Concepts

* Start index is inclusive.
* Stop index is exclusive.
* Negative indices count from the end.
* Negative step can reverse a list.

## Exercises

*Create a list of 5 integers and print the first and last element.
*Create a list A = [10, 20, 30, 40, 50] and print the third element.
*Create a list of fruits and replace "Apple" with "Mango".
*Add "Python" at the end of a list using a list method.
*Insert 100 at index 2 in a list.
*Remove "Delhi" from a list of cities.
*Delete the element at index 3 using a list method.
*Find the length of a list without counting manually.
*Count how many times 5 appears in [1, 5, 2, 5, 3, 5].

## Key Learnings

* Lists are mutable and can be modified after creation.
* Python provides many built-in methods to manage list data efficiently.
* Slicing is a powerful way to access subsets of data.
* Lists can store different data types and duplicate values.
* Lists are one of the most important data structures in Python programming.



