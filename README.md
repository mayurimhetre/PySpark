# PySpark DataFrame Operations and Modeling

This repository demonstrates common **Apache Spark (PySpark)** DataFrame operations for data exploration, preprocessing, and modeling, including imputation and logistic regression.

---

## Displaying DataFrame Values

To view the contents of a Spark DataFrame, use the `show()` method.

```python
df.show()
```

To prevent truncation of column values:
df.show(truncate=False)

# PySpark DataFrame & Machine Learning Concepts

## Displaying DataFrame Values
Used to view rows of a PySpark DataFrame in a tabular format for quick inspection of the data.

## Distinct Count
Calculates the number of unique values present in a specific column of a DataFrame.
```python
df.select("column_name").distinct().count()
```

## Value Count
Counts the frequency of each unique value in a column to understand data distribution.
```python
df.groupBy("column_name").count()
```

## Group By
Groups rows based on one or more columns and applies aggregate functions such as count, sum, or average.
```python
df.groupBy("column_name").count().orderBy("count", ascending=False)
```

## Imputer Technique
Handles missing values in numerical columns by replacing them with statistical measures like mean, median, or mode.
```python
from pyspark.ml.feature import Imputer

imputer = Imputer(
    inputCols=["feature1", "feature2"],
    outputCols=["feature1_imputed", "feature2_imputed"]
)

df_imputed = imputer.fit(df).transform(df)
```

## Logistic Regression
A supervised machine learning algorithm used for binary classification problems by modeling the probability of class membership.
