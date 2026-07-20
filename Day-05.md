# Day 05 - Dictionaries in Python

[Open Google Colab Notebook](https://colab.research.google.com/drive/1NRE89CD4ol6aq1Zn8ySSoJbGwIBYfu8q?usp=sharing)

## Introduction

A Python dictionary is a collection of key-value pairs.

- Dictionaries are enclosed in curly braces `{}`.
- Keys must be unique and immutable.
- Values can be of any data type.
- Dictionaries are unordered collections.
- Dictionaries are also known as mappings in Python.

---

## Creating a Dictionary

```python
dis = {
    'name': 'red',
    'age': 10
}

print(dis)
```

### Output

```python
{'name': 'red', 'age': 10}
```

---

## Accessing Values

```python
print(dis['name'])
```

### Output

```python
red
```

---

## Getting Keys and Values

### Values

```python
print(list(dis.values()))
```

### Output

```python
['red', 10]
```

### Keys

```python
print(dis.keys())
```

### Output

```python
dict_keys(['name', 'age'])
```

---

# Rules for Creating a Dictionary

1. Every key must be unique.
2. Keys must be immutable (string, number, tuple).
3. Dictionary keys have no fixed order.
4. Values can be of any data type.

---

# Methods of Creating Dictionaries

## 1. Literal Syntax

```python
d = {}
d = {'key': 'value'}
```

---

## 2. Dictionary Comprehension

```python
d = {k:v for k,v in [('key', 'value')]}
print(d)
```

### Output

```python
{'key': 'value'}
```

Example:

```python
d = {1: "Mukta" for k,v in [('key', 'value')]}
print(d)
```

### Output

```python
{1: 'Mukta'}
```

---

## 3. Using dict() Constructor

```python
d = dict()
```

### With Keyword Arguments

```python
d = dict(key='value')
print(d)
```

### Output

```python
{'key': 'value'}
```

### Using List of Tuples

```python
d = dict([('Name', 'Diksha'), ('Age', '21')])
print(d)
```

### Output

```python
{'Name': 'Diksha', 'Age': '21'}
```

---

# Modifying a Dictionary

## Adding New Key-Value Pair

```python
d['H.No'] = 42
print(d)
```

---

## Adding a List as Value

```python
d['new_list'] = [1, 2, 3]
```

---

## Adding a Dictionary as Value

```python
d['new_dict'] = {'nested_dict': 1}
```

---

## Deleting a Key

```python
del d['H.No']
```

---

# Built-in Dictionary Methods

## 1. clear()

Removes all items from the dictionary.

```python
my_dict = {
    '1': 'MUKTA',
    '2': 'DIKSHA',
    '3': 'NISHTHA'
}

my_dict.clear()

print(my_dict)
```

### Output

```python
{}
```

---

## 2. get()

Returns value for a key without causing an error if key doesn't exist.

```python
d = {
    'Name': 'Ram',
    'Age': '19',
    'Country': 'India'
}

print(d.get('Name'))
print(d.get('Gender'))
```

### Output

```python
Ram
None
```

---

## 3. items()

Returns all key-value pairs.

```python
d = {
    'Name': 'Ram',
    'Age': '19',
    'Country': 'India'
}

print(d.items())
```

### Output

```python
dict_items([
('Name', 'Ram'),
('Age', '19'),
('Country', 'India')
])
```

---

## 4. keys()

Returns all keys.

```python
print(d.keys())
```

### Output

```python
dict_keys(['Name', 'Age', 'Country'])
```

---

## 5. values()

Returns all values.

```python
print(d.values())
```

### Output

```python
dict_values(['Ram', '19', 'India'])
```

---

## 6. update()

Updates dictionary using another dictionary.

```python
d1 = {
    'Name': 'Ram',
    'Age': '19',
    'Country': 'India'
}

d2 = {
    'Name': 'Neha',
    'Age': '22'
}

d1.update(d2)

print(d1)
```

### Output

```python
{'Name': 'Neha', 'Age': '22', 'Country': 'India'}
```

---

## 7. pop()

Removes and returns the value associated with a specified key.

```python
d = {
    'Name': 'Ram',
    'Age': '19',
    'Country': 'India'
}

d.pop('Age')

print(d)
```

### Output

```python
{'Name': 'Ram', 'Country': 'India'}
```

---

## 8. popitem()

Removes and returns the last inserted key-value pair.

```python
d = {
    'Name': 'Ram',
    'Age': '19',
    'Country': 'India',
    'Gender': 'Male'
}

d.popitem()

print(d)
```

### Output

```python
{'Name': 'Ram', 'Age': '19', 'Country': 'India'}
```

---

## Error Example

```python
d = {}

d.popitem()
```

### Output

```python
KeyError: 'popitem(): dictionary is empty'
```

### Why this Error Occurs?

`popitem()` cannot remove an item from an empty dictionary.

---

# Dictionary Comprehension

## Squares from 1 to 10

```python
squares = {x: x*x for x in range(1,11)}

print(squares)
```

### Output

```python
{
1:1,
2:4,
3:9,
...
10:100
}
```

---

## Even Squares Only

```python
even_squares = {
    x: x*x
    for x in range(1,11)
    if x % 2 == 0
}
```

---

# Nested Dictionaries

```python
school = {
    'Student1': {
        'Name': 'Ram',
        'Age': 19
    },

    'Student2': {
        'Name': 'Neha',
        'Age': 20
    }
}

print(school['Student1']['Name'])
```

### Output

```python
Ram
```

---

# Useful Functions

## Length of Dictionary

```python
print(len(school))
```

### Output

```python
2
```

---

## Sorting Dictionary Keys

```python
d = {
    'c': 3,
    'a': 1,
    'b': 2
}

print(sorted(d.keys()))
```

### Output

```python
['a', 'b', 'c']
```

---

# Advantages of Dictionaries

- Fast lookup using keys.
- Easy storage of related data.
- Supports nested structures.
- Flexible and dynamic.

---

# Summary

In this lesson, we learned:

- Creating dictionaries
- Accessing dictionary values
- Dictionary rules
- Dictionary comprehension
- Modifying dictionaries
- Built-in methods:
  - clear()
  - get()
  - items()
  - keys()
  - values()
  - update()
  - pop()
  - popitem()
- Nested dictionaries
- Sorting dictionaries
- Dictionary applications

---

# Practice Questions

### Basic Dictionary Operations

1. Create a dictionary named `student` with keys:
   - name
   - age
   - grade

2. Print the age.

3. Update the grade.

4. Add a new key called subject.

---

### Dictionary Manipulation

1. Create two dictionaries.
2. Merge them.
3. Remove a key.
4. Check if a key exists.

---

### Dictionary Comprehension

1. Create a dictionary of squares from 1 to 10.
2. Filter only even squares.

---

### Nested Dictionaries

1. Create a school dictionary with multiple students.
2. Access a specific student's information.

---

### Dictionary Methods

1. Use `get()`.
2. Use `pop()`.
3. Use `update()`.
4. Use `items()`.
5. Use `keys()`.
6. Use `values()`.

---

### Real-World Applications

1. Student Management System
2. Employee Records
3. Product Catalogs
4. Contact Lists
5. JSON Data Handling
