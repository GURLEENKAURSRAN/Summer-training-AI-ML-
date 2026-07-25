# 📅 Day-08 Conditional Statements 

[Open Google Notebook](https://colab.research.google.com/drive/1iwmyPu2rUX9v1BirUUMKg80PgW5HINGZ?usp=sharing)

## 📖 Topic Covered

Today I learned **Conditional Statements** in Python, which are used to make decisions in a program. They allow the program to execute different blocks of code depending on whether a condition is `True` or `False`.


# 📘 What are Conditional Statements?

Conditional statements are decision-making statements that control the flow of a program. Instead of executing every line of code sequentially, the program checks a condition and decides which block of code should run.

### **Syntax**

```python
if condition:
    # code executes if condition is True
```

If the condition evaluates to `True`, the code inside the `if` block executes. Otherwise, it is skipped.


# Types of Conditional Statements

## 1. `if` Statement

The `if` statement executes a block of code only when the given condition is `True`.

### Example

```python
age = 18

if age >= 18:
    print("You are eligible to vote.")
```

**Output**

```
You are eligible to vote.
```


## 2. `if...else` Statement

The `if...else` statement provides two possible outcomes.

* If the condition is `True`, the `if` block executes.
* Otherwise, the `else` block executes.

### Example

```python
age = 16

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

**Output**

```
Minor
```

## 3. `if...elif` Statement

When there are multiple conditions to check, `elif` (else if) is used.

### Example

```python
marks = 82

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
```

**Output**

```
Grade B
```

## 4. `if...elif...else` Statement

If none of the conditions are true, the `else` block executes.

### Example

```python
marks = 60

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
else:
    print("Grade C")
```

**Output**

```
Grade C
```

## 5. Nested `if` Statement

A nested `if` means placing one `if` statement inside another `if` statement.

### Example

```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("Entry Allowed")
```

**Output**

```
Entry Allowed
```

# Operators Used in Conditional Statements

### Comparison Operators

| Operator | Meaning                  |
| -------- | ------------------------ |
| `==`     | Equal to                 |
| `!=`     | Not equal to             |
| `>`      | Greater than             |
| `<`      | Less than                |
| `>=`     | Greater than or equal to |
| `<=`     | Less than or equal to    |

### Logical Operators

| Operator | Meaning                             |
| -------- | ----------------------------------- |
| `and`    | Both conditions must be True        |
| `or`     | At least one condition must be True |
| `not`    | Reverses the result                 |


# 💻 Programs Practiced

* Adult or Minor checker
* Even or Odd checker
* Grade Calculator
* Leap Year Checker
* Vowel or Consonant Checker
* Weekend or Weekday Checker
* Positive, Negative, or Zero checker
* Largest of Three Numbers
* FizzBuzz
* Password Validation
* Traffic Light System
* Fuel Level Checker
* BMI Calculator
* Attendance Checker


Conditional statements are one of the most important programming concepts because they allow programs to make intelligent decisions. They form the foundation for building interactive applications, games, automation scripts, and problem-solving algorithms.


