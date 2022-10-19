# 10 minutes to pandas

**Pandas is a game-changer for data science and analytics, particularly if you came to Python because you were searching for something more powerful than Excel and VBA. Pandas uses fast, flexible, and expressive data structures designed to make working with relational or labeled data both easy and intuitive.**

## What kind of data does pandas handle?

- To load the pandas package and start working with it, import the package. The community agreed alias for pandas is pd, so loading pandas as pd is assumed standard practice for all of the pandas documentation.

### How do I read and write tabular data?

- i want to analyze the Titanic passenger data, available as a CSV file.

> titanic = pd.read_csv("data/titanic.csv")

##### pandas provides the read_csv() function to read data stored as a csv file into a pandas DataFrame. pandas supports many different file formats or data sources out of the box (csv, excel, sql, json, parquet, …), each of them with the prefix read_*.

### How to handle time series data with ease?

**Initially, the values in datetime are character strings and do not provide any datetime operations (e.g. extract the year, day of the week,…). By applying the to_datetime function, pandas interprets the strings and convert these to datetime (i.e. datetime64[ns, UTC]) objects. In pandas we call these datetime objects similar to datetime.datetime from the standard library as pandas.Timestamp.**

### How to manipulate textual data?

**To make each of the strings in the Name column lowercase, select the Name column (see the tutorial on selection of data), add the str accessor and apply the lower method. As such, each of the strings is converted element-wise.**

**Similar to datetime objects in the time series tutorial having a dt accessor, a number of specialized string methods are available when using the str accessor. These methods have in general matching names with the equivalent built-in string methods for single elements, but are applied element-wise (remember element-wise calculations?) on each of the values of the columns.**



