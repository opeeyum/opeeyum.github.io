---
layout: template
author: Omprakash
date: 2022-07-06
category: Python

sidebar:
  - name: Pandas
    key: comments
  - name: Series & DataFrames
    key: data-types-in-python
  - name: Creating a DataFrame
    key: operators
  - name: Indexing
    key: conditonal-statement
  - name: Loops
    key: loops
  - name: Basic Data Structures
    key: basic-data-structures
  - name: Functions
    key: functions

dataFrame:
    - name: 14
      key: 165
    - name: 15
      key: 166
    - name: 16
      key: 167
    - name: 17
      key: 168
    - name: 18
      key: 169
---
# Python Pandas Module
<hr>

### What is Pandas?
**Pandas** is one of the most popular data science libraries in Python. Easy to use, it is built on the top of **Numpy** and shares many functions and Properties.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```python
import pandas as pd
```
</div>

### Series and DataFrames
The two primary components of pandas are the **Series** and the **DataFrame**.

A **Series** is essentially a column, and a **DataFrame** is a multidimensinal table made up of a collection of Series.

For example, the following DataFrame is made of two Series, **ages** and **heights**.
<table class = "table table-info table-sm table-bordered align-middle">
    <thead>
        <tr>
        <th>Ages</th>
        <th>Heights</th>
        </tr>
    </thead>
    <tbody>
    {% for item in page.dataFrame %}
        <tr>
            <td>{{item.name}}</td>
            <td>{{item.key}}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

- Series are one-dimensional array.
- DataFrame is a multi-dimensional array.

`Array: List of homogeneous data types.`

### Creating a DataFrame

The easiest way to create a DataFrame is using a **Python Dictionary**.

<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
data = {
    'ages': [14, 18, 24, 42],
    'heights': [165, 180, 176, 184,]
}
```
</div>
- Each key is a column, while the value is an *array* representing the data for that columns.

Now, we can pass this *dictionary* to the DataFrame *constructor*.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
df = pd.DataFrame(data)
```
</div>

- The DataFrame automatically creates a numeric **index** for each row. We can specify a custom index, when creating the DataFrame:
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
df = pd.DataFrame(data, index = ['Op', 'NK', 'AKD', 'TC'])
```
</div>

- We can access a row using its index and the **`loc[]`** function:
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
print(df.loc["NK"])
```
</div>

### Indexing

We can select a single column by specifying its name in square brackets:

<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
print(df['ages'])
```
</div>

- If we want to select multiple columns, we can specify a list of column names:
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
print(df[['ages', 'heights']])
```
</div>

### Slicing 
Pandas uses the **`iloc`** function to select data based on its numeric index. It works the same way indexing lists does in python.

<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
print(df.iloc[2])

print(df.iloc[:3])

print(df.iloc[1:3])
```
</div>

### Conditons
We can also selects the data based on a conditon.

For example, lets select all rows where **age** is greater than 18 and **height** is greater than 180.

<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
df[(df['ages'] > 18) & (df[heights] > 180)]
```
</div>

- Similary, the or `|` operator can be used to combine conditions.

### Reading Data
It is quite common for data to come in a file format. One of the most popular formats is the **CSV**.

Pandas supports reading data from a CSV file directly into a DataFrame.

The **`read_csv()`** function reads the data of a CSV file into a DataFrame:
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>

```py
df = pd.read_csv(<file path>)
```
</div>