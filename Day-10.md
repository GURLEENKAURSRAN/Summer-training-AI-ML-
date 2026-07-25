# Day-10 - while Loop, Infinite Loop, Loop Control Statements & Nested Loops

[Open Google Colab Notebook](https://colab.research.google.com/drive/1cq2c1Vqi62yQiAlqXfDx96AxGrgJUCvY?usp=sharing)

## Topic Covered

Today I learned about the **`while` loop**, **Infinite Loops**, **Loop Control Statements (`break`, `continue`, `pass`)**, and **Nested Loops** in Python. These concepts help control how loops execute and solve more complex programming problems.

---

# 1. `while` Loop

A **`while` loop** repeatedly executes a block of code **as long as the given condition is `True`**. It is mainly used when the number of iterations is **not known in advance**.

### Syntax

```python
while condition:
    # code to execute
```

### Example

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

**Output**

```
1
2
3
4
5
```

### When to Use

* Taking user input until a valid value is entered.
* Menu-driven programs.
* Repeating tasks until a condition becomes false.

# 2. Infinite Loop

An **Infinite Loop** occurs when the loop condition **never becomes `False`**, causing the program to run forever.

### Example

```python
while True:
    print("Running...")
```

### Important Points

* Used carefully in games, servers, and continuously running applications.
* Usually terminated using a `break` statement or user action (`Ctrl + C`).

# 3. Loop Control Statements

Loop control statements change the normal execution flow of a loop.

## a) `break`

The `break` statement **immediately terminates the loop**, even if more iterations remain.

### Example

```python
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```

**Output**

```
1
2
```

### Use Cases

* Searching for an item.
* Exiting a loop once the required condition is met.

## b) `continue`

The `continue` statement **skips the current iteration** and moves to the next iteration.

### Example

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

**Output**

```
1
2
4
5
```

### Use Cases

* Ignoring unwanted values.
* Filtering data while continuing the loop.

---

## c) `pass`

The `pass` statement **does nothing**. It is used as a placeholder where Python expects a statement.

### Example

```python
for ch in "Python":
    if ch == "o":
        pass
```

### Use Cases

* Creating empty functions or loops during development.
* Avoiding syntax errors while writing incomplete code.

---

#  4. Nested Loops

A **Nested Loop** is a loop inside another loop. For every iteration of the outer loop, the inner loop executes completely.

### Syntax

```python
for i in range(rows):
    for j in range(columns):
        # code
```

### Example

```python
for i in range(3):
    for j in range(4):
        print(j)
```

### Applications

* Pattern printing
* Multiplication tables
* Matrix operations
* Working with two-dimensional data

---

#  Programs Practiced

### While Loop

* Print numbers from 1 to 10
* Reverse counting
* Print odd and even numbers
* Multiplication table
* Factorial using `while`
* Sum of digits
* Reverse a number
* Check palindrome number
* Prime number checking
* Largest digit in a number
* Calculate power without using the power operator

### Loop Control Statements

* Stop a loop using `break`
* Skip values using `continue`
* Use `pass` as a placeholder
* Keep taking input until the user enters `"exit"`


#  Key Learnings

* `while` loops are useful when the number of iterations is unknown.
* Infinite loops occur when the loop condition never becomes false.
* `break` exits a loop immediately.
* `continue` skips only the current iteration.
* `pass` acts as a placeholder without affecting execution.
* Nested loops execute the inner loop completely for every iteration of the outer loop.

