# Panda library

Pandas is an open-source library that is made mainly for working with relational or labeled data both easily and intuitively. It provides various data structures and operations for manipulating numerical data and time series. This library is built on top of the NumPy library. Pandas is fast and it has high performance & productivity for users.

The primary two components of pandas are the Series and DataFrame.

![series-and-dataframe](pic/series-and-dataframe.png "series-and-dataframe")

There are many ways to create a DataFrame from scratch, but a great option is to just use a simple dict.
And then pass it to the pandas DataFrame constructor :

    data = {
        'apples': [3, 2, 0, 1], 
        'oranges': [0, 3, 7, 2]
    }

    purchases = pd.DataFrame(data)

    purchases
Exploring, cleaning, transforming, and visualization data with pandas in Python is an essential skill in data science
