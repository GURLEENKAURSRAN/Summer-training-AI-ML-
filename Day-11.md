# Day-11 Daily Diary – Functions in Python

[Open Google Colab Notebook](https://colab.research.google.com/drive/16t5U6Lu7V-PHg6BP94febf0PcAqvEm4-?usp=sharing)

## Topic Covered

Today I learned about **Functions** in Python. Functions are reusable blocks of code designed to perform a specific task. Instead of writing the same code multiple times, we can write it once inside a function and call it whenever needed.

---

# What is a Function?

A **function** is a named block of code that performs a particular task. Functions help make programs modular, organized, and easier to understand.

### Why Do We Use Functions?

* **Code Reusability** – Write the code once and use it multiple times.
* **Better Readability** – Programs become easier to understand.
* **Easy Maintenance** – Changes need to be made in only one place.
* **Reduced Code Duplication** – Avoids writing the same code repeatedly.
* **Modular Programming** – Breaks large programs into smaller, manageable parts.

---

# Syntax of a Function

```python
def function_name(parameters):
    # function body
```

### Components

* `def` → Keyword used to define a function.
* `function_name` → Name of the function.
* `parameters` → Input values accepted by the function.
* Function body → Code that performs the required task.

---

# Defining and Calling a Function

### Example

```python
def greet(name):
    print(f"Welcome {name}!")

greet("Gurleen")
```

**Output**

```text
Welcome Gurleen!
```

Here:

* `greet` is the function name.
* `name` is the **parameter**.
* `"Gurleen"` is the **argument** passed during the function call.

---

# Function Arguments

**Arguments** are the actual values passed to a function when it is called. They allow the same function to work with different inputs.

### Example

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

**Output**

```text
30
```

#  Return Statement

The **`return`** statement sends a value back to the function caller. Unlike `print()`, `return` allows the returned value to be stored, reused, or passed to another function.

### Example

```python
def square(n):
    return n * n

result = square(5)
print(result)
```

**Output**

```text
25
```

# Types of Arguments

Python supports different ways of passing arguments to functions.

### 1. Positional Arguments

Arguments are passed in the same order as the parameters.

```python
def intro(name, age):
    print(name, age)

intro("Gurleen", 19)
```

### 2. Keyword Arguments

Arguments are passed using parameter names.

```python
intro(age=19, name="Gurleen")
```

### 3. Default Arguments

A default value is assigned to a parameter if no argument is provided.

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
```

### 4. Variable-Length Arguments

Used when the number of arguments is unknown.

```python
def total(*numbers):
    print(sum(numbers))

total(10, 20, 30, 40)
```

# Variable Scope

**Scope** determines where a variable can be accessed in a program.

### Local Variable

A variable created inside a function. It can only be accessed within that function.

```python
def demo():
    x = 10
    print(x)
```

### Global Variable

A variable declared outside all functions. It can be accessed throughout the program.

```python
x = 100

def demo():
    print(x)

demo()
```

# Programs Practiced

* Greeting function
* Addition using functions
* Square of a number using `return`
* Find maximum number in a list
* Reverse a string
* Count vowels
* Check palindrome
* Check leap year
* Prime number checker
* Average of numbers
* Filter even numbers
* Reverse words in a sentence
* Find long strings in a list
* Programs using positional, keyword, default, and variable-length arguments

#  Key Learnings

* Functions organize code into reusable blocks.
* `def` is used to define a function.
* Parameters receive data, while arguments provide data.
* `return` sends values back to the caller.
* Python supports positional, keyword, default, and variable-length arguments.
* Variables can have local or global scope.
* Functions improve readability, maintainability, and code reusability.

