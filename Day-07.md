# Day 07 – Python String Methods

## Overview

Today's session focused on **Python String Methods**. Strings are one of the most frequently used data types in Python, and built-in string methods make it easy to manipulate, format, search, validate, and transform text efficiently.

## Topics Covered

### 1. String Case Conversion

Learned methods used to change the letter case of strings.

* `capitalize()`
* `casefold()`
* `lower()`
* `upper()`
* `swapcase()`
* `title()`

**Example:**

```python
text = "hello world"

print(text.capitalize())
print(text.upper())
print(text.title())
```

---

### 2. String Searching & Counting

Explored methods used to search for substrings and count occurrences.

* `find()`
* `index()`
* `rfind()`
* `rindex()`
* `count()`
* `startswith()`
* `endswith()`

These methods help locate text within a string and check whether a string starts or ends with a specific sequence.

---

### 3. String Validation Methods

Learned methods that return either `True` or `False` based on the string content.

* `isalnum()`
* `isalpha()`
* `isdigit()`
* `isdecimal()`
* `isnumeric()`
* `isascii()`
* `islower()`
* `isupper()`
* `istitle()`
* `isspace()`
* `isidentifier()`
* `isprintable()`

These methods are useful for validating user input.

---

### 4. String Formatting

Studied different ways to format strings.

* `format()`
* `format_map()`
* `center()`
* `ljust()`
* `rjust()`
* `zfill()`

These methods help create well-formatted output and aligned text.

---

### 5. String Modification Methods

Learned methods that modify or clean string data.

* `replace()`
* `strip()`
* `lstrip()`
* `rstrip()`
* `expandtabs()`
* `translate()`
* `maketrans()`

These methods are commonly used while cleaning and preprocessing text.

---

### 6. Splitting and Joining Strings

Practiced methods used to break strings into smaller parts or combine multiple strings.

* `split()`
* `rsplit()`
* `splitlines()`
* `partition()`
* `rpartition()`
* `join()`

These methods are especially useful when working with files, CSV data, and user input.

---

### 7. Encoding Strings

Learned about:

* `encode()`

This method converts a string into bytes using a specified encoding such as UTF-8.

---

## Practice Questions: 

* Changing the case of strings.
* Searching for substrings.
* Counting character occurrences.
* Replacing text.
* Splitting and joining strings.
* Removing extra spaces.
* Validating different types of input.
* Formatting strings for better output.
* Creating translation tables using `maketrans()` and `translate()`.

---



