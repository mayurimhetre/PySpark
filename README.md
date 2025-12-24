# PySpark DataFrame Operations and Modeling

This repository demonstrates common **Apache Spark (PySpark)** DataFrame operations for data exploration, preprocessing, and modeling, including imputation and logistic regression.

---

## Displaying DataFrame Values

To view the contents of a Spark DataFrame, use the `show()` method.

```python
df.show()
---
To prevent truncation of column values:
```python
df.show(truncate=False)

# PySpark DataFrame & Machine Learning Concepts

## Displaying DataFrame Values
Used to view rows of a PySpark DataFrame in a tabular format for quick inspection of the data.

## Distinct Count
Calculates the number of unique values present in a specific column of a DataFrame.

## Value Count
Counts the frequency of each unique value in a column to understand data distribution.

## Group By
Groups rows based on one or more columns and applies aggregate functions such as count, sum, or average.

## Imputer Technique
Handles missing values in numerical columns by replacing them with statistical measures like mean, median, or mode.

## Logistic Regression
A supervised machine learning algorithm used for binary classification problems by modeling the probability of class membership.
