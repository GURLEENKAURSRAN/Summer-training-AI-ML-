# Day 04 - Sets in Python

[Open Google Colab Notebook](https://colab.research.google.com/drive/1vKW9HC-a0Nx3j4lnlR3LiNYLRQ53S3mw?usp=sharing).

## Introduction

A Python set is a well-defined collection of distinct objects, called elements or members.

### Key Features of Sets

- Sets are unordered collections.
- Elements in a set are unique.
- Duplicate values are automatically removed.
- Sets are mutable (can be modified).
- Set elements must be immutable (hashable).

There are two types of sets in Python:

1. Set (Mutable)
2. Frozen Set (Immutable)

---

## Creating Sets

### Regular Set

```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
print(basket)
```

### Output

```python
{'orange', 'banana', 'pear', 'apple'}
```

Duplicates are removed automatically.

### Creating a Set from a String

```python
a = set('abracadabra')
print(a)
```

### Output

```python
{'c', 'r', 'b', 'd', 'a'}
```

---

## Frozen Sets

A frozen set is an immutable version of a set.

```python
b = frozenset('asdfagsa')
print(b)
```

### Output

```python
frozenset({'g', 'f', 'd', 's', 'a'})
```

### Example

```python
cities = frozenset(["Frankfurt", "Basel", "Freiburg"])
print(cities)
```

### Output

```python
frozenset({'Frankfurt', 'Freiburg', 'Basel'})
```

---

# Set Operations

Assume:

```python
A = {1, 2, 3, 4, 5}
B = {3, 4, 5, 6}
```

## Intersection

Returns common elements.

```python
A.intersection(B)
```

or

```python
A & B
```

### Output

```python
{3, 4, 5}
```

---

## Union

Returns all unique elements.

```python
A.union(B)
```

or

```python
A | B
```

### Output

```python
{1, 2, 3, 4, 5, 6}
```

---

## Difference

Returns elements present in first set but not second.

```python
A.difference(B)
```

or

```python
A - B
```

### Output

```python
{1, 2}
```

---

## Symmetric Difference

Returns elements present in either set but not both.

```python
A.symmetric_difference(B)
```

or

```python
A ^ B
```

### Output

```python
{1, 2, 6}
```

---

## Subset Check

```python
{1, 2}.issubset({1, 2, 3})
```

### Output

```python
True
```

or

```python
{1, 2} <= {1, 2, 3}
```

---

## Superset Check

```python
{1, 2, 3}.issuperset({1, 2})
```

### Output

```python
True
```

or

```python
{1, 2, 3} >= {1, 2}
```

---

## Proper Subset

Incorrect:

```python
{1}.ispropersubset({1,2,3})
```

### Error

```python
AttributeError: 'set' object has no attribute 'ispropersubset'
```

### Correct Way

```python
{1} < {1,2,3}
```

### Output

```python
True
```

---

## Disjoint Sets

Checks whether two sets have no common elements.

```python
{1,2}.isdisjoint({3,4})
```

### Output

```python
True
```

```python
{1,2}.isdisjoint({1,4})
```

### Output

```python
False
```

---

# Operations on Single Elements

## Membership Check

```python
2 in {1,2,3}
```

Output:

```python
True
```

```python
4 not in {1,2,3}
```

Output:

```python
True
```

---

## Add Elements

```python
s = {1,2,3}
s.add(4)
print(s)
```

Output:

```python
{1,2,3,4}
```

---

## Remove Elements

### discard()

```python
s.discard(3)
```

If element doesn't exist, no error occurs.

### remove()

```python
s.remove(2)
```

If element doesn't exist:

```python
KeyError
```

---

## Update Set

```python
s = {1,2}
s.update({3,4})
print(s)
```

Output:

```python
{1,2,3,4}
```

---

# Removing Duplicates Using Sets

```python
restaurants = [
    "McDonald's",
    "Burger King",
    "McDonald's",
    "Chicken Chicken"
]

unique_restaurants = set(restaurants)

print(unique_restaurants)
```

Output:

```python
{'Chicken Chicken', 'Burger King', "McDonald's"}
```

Convert back to list:

```python
list(set(restaurants))
```

---

# Set of Sets

This is invalid:

```python
{{1,2}, {3,4}}
```

### Error

```python
TypeError: unhashable type: 'set'
```

### Correct Way

Use frozenset:

```python
{
    frozenset({1,2}),
    frozenset({3,4})
}
```

Output:

```python
{frozenset({3,4}), frozenset({1,2})}
```

---

# Advantages of Sets

- Automatically remove duplicates
- Fast membership testing
- Efficient mathematical operations
- Useful for data cleaning and analysis

---

# Real-World Applications

### Example 1: Unique Visitors

```python
visitors = [
    "User1",
    "User2",
    "User1",
    "User3"
]

unique_visitors = set(visitors)
```

### Example 2: Removing Duplicate Records

```python
emails = [
    "a@gmail.com",
    "b@gmail.com",
    "a@gmail.com"
]

unique_emails = set(emails)
```

### Set Methods

1. Name three common set methods.
2. How do you add an element to a set?
3. Difference between remove() and discard()?

### Frozen Sets

1. What is a frozen set?
2. How is it different from a regular set?
3. When should you use a frozen set?

### Exercise

1. Create a set containing first five prime numbers.
2. Add 7 to the set.
3. Remove 3 from the set.
4. Check if it is a subset of `{2,3,5,7,11}`.
5. Find union with `{7,11,13}`.
6. Create a frozenset from it.
7. Check if it has common elements with `{1,4,9}`.
8. Clear all elements.
9. Create a set of favorite fruits and find intersection with:

