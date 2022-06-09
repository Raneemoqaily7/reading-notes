
## Introduction to Pandas in Python

Pandas is an open-source library that provides various data structures and operations for manipulating numerical data and time series. This library is built on top of the NumPy library. Pandas is fast and it has high performance & productivity for users, according to its developers.


## Advantages 
1. Fast and efficient for manipulating and analyzing data.
2. Data from different file objects can be loaded.
3. Easy handling of missing data (represented as NaN) in floating point as well as non-floating point data
4. Size mutability: columns can be inserted and deleted from DataFrame and higher dimensional objects
5. Data set merging and joining.
6. Flexible reshaping and pivoting of data sets
7. Provides time-series functionality.
8. Powerful group by functionality for performing split-apply-combine operations on data sets.



## What is Pandas and How does it work ?

Pandas is an open source Python library that allows users to explore, manipulate and visualise data in an extremely efficient manner. It is literally Microsoft Excel in Python.

## Why is Pandas so Popular ?
It is easy to read and learn
It is extremely fast and powerful
It integrates well with other visualisation libraries
It is black, white and asian at the same time

## What kind of data does Pandas take ?
Pandas can take in a huge variety of data, the most common ones are csv, excel, sql or even a webpage.


## Getting Started


- The first step of working in pandas 

`pip install pandas`

- After the pandas have been installed into the system, you need to import the library.

`import pandas as pd`


### Pandas generally provide two data structures for manipulating data, They are: 

- Series
- DataFrame


#### Pandas Series is a one-dimensional array that holds data of any type (integer, string, float, python objects, etc.). Pandas Series supports both integer and label-based indexing and provides a host of methods for performing operations involving the index. The axis labels are collectively called indexes.

- Creating a Series
In the real world, a Pandas Series will be created by loading the datasets from existing storage, storage can be SQL Database, CSV file, an Excel file. Pandas Series can be created from the lists, dictionary, and from a scalar value etc.


Example:

```
import pandas as pd
import numpy as np


# Creating empty series
ser = pd.Series()

print(ser)

# simple array
data = np.array(['g', 'e', 'e', 'k', 's'])

ser = pd.Series(data)
print(ser)

```

Output :

Series([], dtype: float64)
0    g
1    e
2    e
3    k
4    s
dtype: object


Example :
```
import pandas

mydataset = {
  'cars': ["BMW", "Volvo", "Ford"],
  'passings': [3, 7, 2]
}

myvar = pandas.DataFrame(mydataset)

print(myvar)
```

Output : 

```
  cars  passings
0    BMW         3
1  Volvo         7
2   Ford         2
```


## Pandas - Analyzing DataFrames
- head() method ,returns the headers and a specified number of rows, starting from the top.


```
import pandas as pd

df = pd.read_csv('data.csv')

print(df.head(10))
```


Output :


```
 Duration  Pulse  Maxpulse  Calories
0        60    110       130     409.1
1        60    117       145     479.0
2        60    103       135     340.0
3        45    109       175     282.4
4        45    117       148     406.0
5        60    102       127     300.5
6        60    110       136     374.0
7        45    104       134     253.3
8        30    109       133     195.1
9        60     98       124     269.0
```



Example

Print the first 5 rows of the DataFrame:

```
import pandas as pd

df = pd.read_csv('data.csv')

print(df.head())
```

Output 

```
Duration  Pulse  Maxpulse  Calories
0        60    110       130     409.1
1        60    117       145     479.0
2        60    103       135     340.0
3        45    109       175     282.4
4        45    117       148     406.0
```

- tail() method for viewing the last rows of the DataFrame.

Example
```
Print the last 5 rows of the DataFrame:

print(df.tail())
```


Output :

```
Duration  Pulse  Maxpulse  Calories
164        60    105       140     290.8
165        60    110       145     300.4
166        60    115       145     310.2
167        75    120       150     320.4
168        75    125       150     330.4
```



### Info About the Data

 info(), that gives you more information about the data set.

Example

Print information about the data:
```
print(df.info())
```















