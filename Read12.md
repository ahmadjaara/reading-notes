# Panda library

Pandas is an open-source library that is made mainly for working with relational or labeled data both easily and intuitively. It provides various data structures and operations for manipulating numerical data and time series. This library is built on top of the NumPy library. Pandas is fast and it has high performance & productivity for users.

The primary two components of pandas are the Series and DataFrame.

![series-and-dataframe](pic/series-and-dataframe.png "series-and-dataframe")

ex:

    data = {
        'apples': [3, 2, 0, 1], 
        'oranges': [0, 3, 7, 2]
    }

    purchases = pd.DataFrame(data)

    purchases
