# pandas
## What kind of data does pandas handle?
When working with tabular data, such as data stored in spreadsheets or databases, pandas is the right tool for you. pandas will help you to explore, clean and process your data. In pandas, a data table is called a DataFrame.
## DataFrame
A DataFrame is a 2-dimensional data structure that can store data of different types (including characters, integers, floating point values, categorical data and more) in columns. It is similar to a spreadsheet, a SQL table 

- Import the package, aka import pandas as pd
- A table of data is stored as a pandas DataFrame
- Each column in a DataFrame is a Series

## How do I read and write tabular data?
- Getting data in to pandas from many different file formats or data sources is supported by read_* functions.

- Exporting data out of pandas is provided by different to_*methods.

- The head/tail/info methods and the dtypes attribute are convenient for a first check.

## How do I select a subset of a table?

- When selecting subsets of data, square brackets [] are used.

- Inside these brackets, you can use a single column/row label, a list of column/row labels, a slice of labels, a conditional expression or a colon.

- Select specific rows and/or columns using loc when using the row and column names

- Select specific rows and/or columns using iloc when using the positions in the table

- You can assign new values to a selection based on loc/iloc.

## How to create new columns derived from existing columns?
- Create a new column by assigning the output to the DataFrame with a new column name in between the [].

- Operations are element-wise, no need to loop over rows.

- Use rename with a dictionary or function to rename row labels or column names.

## How to calculate summary statistics?
- Aggregation statistics can be calculated on entire columns or rows

- groupby provides the power of the split-apply-combine pattern

- value_counts is a convenient shortcut to count the number of entries in each category of a variable


