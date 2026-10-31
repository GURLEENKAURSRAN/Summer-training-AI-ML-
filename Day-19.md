# Day 19 – Machine Learning: Linear Regression


## Overview

I learned about **Linear Regression**, which is a supervised Machine Learning algorithm used to predict continuous numerical values.

I understood how Linear Regression works, its main objective, the concept of the best-fit line, the Least Squares Method, and the mathematical equation used for prediction.

## Topics Covered

### 1. Introduction to Linear Regression

Linear Regression is a supervised Machine Learning algorithm used to find the relationship between an independent variable and a dependent variable.

It is mainly used for predicting continuous values such as:
- House prices
- Student marks
- Salary
- Temperature
- Height prediction

### 2. Goal of Linear Regression

The main goal of Linear Regression is to find the **best-fit line** that represents the relationship between the given data points.

For example, suppose we have a dataset containing:
- Father's height on the X-axis (independent variable).
- Son's height on the Y-axis (dependent variable).

We can use Linear Regression to predict the son's height based on the father's height.

The algorithm tries to find a line that minimizes the vertical distance between the actual data points and the predicted values on the line.

### 3. Best-Fit Line

A best-fit line is the line that represents the overall relationship between the data points as accurately as possible.

To find the most suitable line, Linear Regression uses the Least Squares Method.

### 4. Least Squares Method

The Least Squares Method is used to find the best-fit line by minimizing the sum of the squared residuals.

**Residual:** The difference between the actual value and the predicted value.

\[
Residual = Actual\ Value - Predicted\ Value
\]

The method calculates the squared residuals and finds the line for which their total is minimum.

\[
SSE = \sum (y_i-\hat{y}_i)^2
\]

Where:
- \(y_i\) = Actual value
- \(\hat{y}_i\) = Predicted value
- SSE = Sum of Squared Errors

### 5. Linear Regression Equation

The mathematical equation of Simple Linear Regression is:

\[
y = mx + c
\]

It can also be written as:

\[
y = \alpha_0 + \alpha_1x
\]

Where:

- **x:** Independent variable (input).
- **y:** Dependent variable (output).
- **m / α₁:** Slope of the line.
- **c / α₀:** Intercept of the line.

### 6. Understanding Slope and Intercept

**Slope (m):**
- Represents the change in the predicted value of y when x increases by one unit.
- A positive slope indicates an increasing relationship.
- A negative slope indicates a decreasing relationship.

**Intercept (c):**
- Represents the predicted value of y when x is zero.
- It is the point where the line crosses the Y-axis.

### 7. Simple Python Example

We can use Python to create a simple linear relationship and visualize it using Matplotlib.

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

plt.scatter(x, y)
plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Data Points")
plt.show()
```

This code creates a scatter plot to display the relationship between two variables.

## Key Learnings

1. Understood the concept of Machine Learning and Linear Regression.
2. Learned that Linear Regression is used for predicting continuous numerical values.
3. Understood independent and dependent variables.
4. Learned the objective of finding the best-fit line.
5. Understood the Least Squares Method.
6. Learned the concept of residuals and squared errors.
7. Understood the Linear Regression equation.
8. Learned the meaning of slope and intercept.
9. Explored the relationship between data points using a scatter plot.

## Practice Questions

1. What is Linear Regression?
2. Why is Linear Regression used in Machine Learning?
3. What is the difference between an independent and dependent variable?
4. What is the main goal of Linear Regression?
5. What is a best-fit line?
6. What is the Least Squares Method?
7. What is a residual in Linear Regression?
8. Write the mathematical equation of Linear Regression.
9. What is the meaning of slope and intercept?
10. What is the difference between a positive and negative slope?
11. What is the difference between actual and predicted values?
12. Give three real-life applications of Linear Regression.

