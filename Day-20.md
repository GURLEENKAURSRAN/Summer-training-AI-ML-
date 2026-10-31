# Day 20 – Machine Learning: Logistic Regression

## Overview

I learned about **Logistic Regression**, a supervised Machine Learning algorithm mainly used for classification problems.

I understood how Logistic Regression is used for binary classification, how the Sigmoid Function converts values into probabilities, how the classification threshold works, and how to evaluate predictions using a Confusion Matrix.

## Topics Covered

### 1. Introduction to Logistic Regression

Logistic Regression is a supervised Machine Learning algorithm used to predict categorical outcomes.

It is mainly used for classification problems where the output belongs to a particular class.

### 2. Logistic Regression for Classification

Logistic Regression is commonly used for binary classification, where the output contains two possible classes: 0 and 1.

**Real-life examples:**

- **Spam vs Ham Email:** Classifying an email as spam (1) or not spam (0).
- **Loan Default:** Predicting whether a person will default on a loan (1) or not (0).
- **Disease Diagnosis:** Predicting whether a person has a disease (1) or does not have a disease (0).

### 3. Why Not Use Linear Regression for Classification?

Linear Regression is mainly used to predict continuous numerical values.

For binary classification, its predictions can fall below 0 or above 1, which makes them unsuitable as probabilities.

Instead, Logistic Regression transforms the linear output using the Sigmoid Function to produce values between 0 and 1.

### 4. Sigmoid Function

The Sigmoid Function is an important part of Logistic Regression.

It takes any real-valued input and converts it into a value between 0 and 1.

\[
\sigma(z)=\frac{1}{1+e^{-z}}
\]

Where:
- \(z\) = Input value from the linear model.
- \(e\) = Euler's number.
- \(\sigma(z)\) = Output probability.

The output can be interpreted as the probability of belonging to class 1.

### 5. Classification Threshold

A classification threshold is used to convert predicted probabilities into class labels.

The commonly used threshold is **0.5**.

- If probability is greater than or equal to 0.5, the predicted class is 1.
- If probability is less than 0.5, the predicted class is 0.

**Example:**

| Predicted Probability | Predicted Class |
|---|---|
| 0.85 | 1 |
| 0.70 | 1 |
| 0.40 | 0 |
| 0.15 | 0 |

This helps convert probability values into final classification results.

### 6. Error Metrics

Error metrics are used to evaluate the performance of a classification model.

One important evaluation tool used in Logistic Regression is the **Confusion Matrix**.

### 7. Confusion Matrix

A Confusion Matrix is a table used to compare actual class labels with predicted class labels.

It helps us understand how correctly a classification model makes predictions.

### 8. Basic Terminology of Confusion Matrix

There are four important terms:

**1. True Positive (TP)**
- The actual class is positive (1).
- The model correctly predicts positive (1).

**2. True Negative (TN)**
- The actual class is negative (0).
- The model correctly predicts negative (0).

**3. False Positive (FP)**
- The actual class is negative (0).
- The model incorrectly predicts positive (1).
- Also called a Type I Error.

**4. False Negative (FN)**
- The actual class is positive (1).
- The model incorrectly predicts negative (0).
- Also called a Type II Error.

### 9. Confusion Matrix Structure

|  | Predicted Positive (1) | Predicted Negative (0) |
|---|---|---|
| Actual Positive (1) | True Positive (TP) | False Negative (FN) |
| Actual Negative (0) | False Positive (FP) | True Negative (TN) |

This matrix helps identify correct and incorrect predictions made by the model.

## Key Learnings

1. Understood the concept of Logistic Regression.
2. Learned that Logistic Regression is used for classification problems.
3. Understood binary classification using classes 0 and 1.
4. Learned why Linear Regression is not suitable for binary classification.
5. Understood the working of the Sigmoid Function.
6. Learned how probabilities are converted into class labels using a threshold.
7. Understood the importance of classification evaluation.
8. Learned the structure and purpose of a Confusion Matrix.
9. Understood True Positive, True Negative, False Positive, and False Negative.

## Practice Questions

1. What is Logistic Regression?
2. Why is Logistic Regression used for classification?
3. What is binary classification?
4. Give three real-life applications of Logistic Regression.
5. Why can't Linear Regression be directly used for binary classification?
6. What is the Sigmoid Function?
7. What is the output range of the Sigmoid Function?
8. What is a classification threshold?
9. What happens when the predicted probability is below 0.5?
10. What is a Confusion Matrix?
11. Define True Positive and True Negative.
12. Define False Positive and False Negative.

