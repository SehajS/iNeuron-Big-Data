# Pandas Assignment

Q1. How do you load a CSV file into a Pandas DataFrame?

A1. One can read the csv file into a DataFrame using the following syntax
```{python}
df = pd.read_csv('filename.csv')
```

Q2. How do you check the data type of a column in a Pandas DataFrame?

A2. For a column name `col_name` in the DataFrame `df`, the data type of the column can be checked using the following syntax
```{python}
df['col_name'].dtypes
```

Q3. How do you select rows from a Pandas DataFrame based on a condition?

A3. In order to select rows from a Pandas DataFrame that satisfy a certain condition, say having a column `cond_col` being equal to value `val`, one can use the following syntax:
```{python}
df = df[df['cond_col'] == val]
```

In general, the above syntax can be generalized to any logical expression. The generalized pseudocode is:
```
df = df[logical expression on df['cond_col']]
```

Q4. How do you rename columns in a Pandas DataFrame?

A4. To rename a column `old_col_name` to the `new_col_name` in a Pandas DataFrame `df`, one can use `rename()` method as shown below:
```{python}
df = df.rename(columns={'old_col_name': 'new_col_name'})
```

Q5. How do you drop columns in a Pandas DataFrame?

A5. To drop a list of columns `drop_list` from a Pandas DataFrame `df`, one can the following syntax:

```{python}
df = df.drop(drop_list, axis=1)
```

Q6. How do you find the unique values in a column of a Pandas DataFrame?

A6. There are two ways to find unique values in a column of Pandas DataFrame as shown below:

```{python}
# option 1 - using the set data structure
set(df['col_name'])

# option 2 - using unique() method
df['col_name'].unique()
```

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?

A7. The number of missing values in each column of a Pandas DataFrame can be found using the following syntax:

```{python}
df.isna().sum()

# another way
df.isnull().sum()
```

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?

A8. To fill missing values in a Pandas DataFrame with a specific value (say 0 for demonstration purposes), one call use `fillna()` as shown below:

```{python}
df = df.fillna(0)
```

Q9. How do you concatenate two Pandas DataFrames?

A9. One can concat two Pandas DataFrames, `df1` and `df2`, using `pd.concat()` function as shown below:

```{python}
# concatenating along rows
df3 = pd.concat([df1, df2])

# concatenating along columns
df3 = pd.concat([df1, df2], axis=1)
```

Q10. How do you merge two Pandas DataFrames on a specific column?

A10. Depending upon the type of join one would like to perform (by default, it is inner join), two dataframes `df1` and `df2` can be merged on the column `col_name` using the following syntax:

```{python}
df = pd.merge(df1, df2, on='col_name', how='inner')
```

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?

A11. To group the data by a column `group_col_name` and then to get an aggreation (say mean for demonstration purposes) by another column `agg_col_name`, one can utilize the following syntax:

```{python}
group_df = df.groupby('group_col_name').agg({'agg_col_name':np.mean})
```

Q12. How do you pivot a Pandas DataFrame?

Q13. How do you change the data type of a column in a Pandas DataFrame?

A13. To change the data type of a column `col_name` in a Pandas DataFrame `df`, one can use the `astype()` method as shown below:

```{python}
# for demonstration purposes, one will convert it to str data type
df['col_name'] = df['col_name'].astype(str)
```

Q14. How do you sort a Pandas DataFrame by a specific column?

A14. To sort a Pandas DataFrame one can utilize `sort_values()` as shown below:

```{python}
df = df.sort_values(by='col_name')
```

Q15. How do you create a copy of a Pandas DataFrame?

A15. One can use `copy()` method to create a copy of a Pandas DataFrame as shown below:

```{python}
df_copy = df.copy()
```

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?

Q17. How do you calculate the mean of a column in a Pandas DataFrame?

A17. One can use `.mean()` method to calcualte the mean of a column in a Pandas DataFrame as shown below:

```{python}
mean_val = df['col_name'].mean()
```

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?

A18. One can use `.std()` method to calcualte the standard deviation of a column in a Pandas DataFrame as shown below:

```{python}
std_val = df['col_name'].std()
```

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?

A19. In order to find correlation between two columns, `col_1` and `col_2` in a Pandas DataFrame `df`, one can utilize the `corr()` method as shown below:
```{python}
corr_value = df['col_1'].corr(df['col_2'])
```

Q20. How do you select specific columns in a DataFrame using their labels?

A20. In order to select a list of columns, say `col_list` from a Pandas DataFrame, all one has to do is enclose them in square brackets as shown below:
```{python}
df[col_list]
```

Q21. How do you select specific rows in a DataFrame using their indexes?

A21. Using iloc one can select specfic rows using their indexes. All one has to do is enclose the list of indexes, say `index_list` in square brackets as shown below:
```{python}
df.iloc[index_list]
```

Q22. How do you sort a DataFrame by a specific column?

A22. To sort a Pandas DataFrame one can utilize `sort_values()` as shown below:

```{python}
df = df.sort_values(by='col_name')
```

Q23. How do you create a new column in a DataFrame based on the values of another column?

A23. Pandas is built on top of NumPy and thus allows for vectorization of operations while creating new columns. All one has to do is to use [] to create a new column. All the operations are element-wise and there are no loops required. Below is an example:

```{python}
# create a new column the elements of whom are sum of other two columns 
df['sum'] = df['col_1'] + df['col_2']
```

Q24. How do you remove duplicates from a DataFrame?

A24. In order to remove duplicates from a Pandas DataFrame, one can utilize the `drop_duplicates()` function as shown below:
```{python}
# use this if you want to remove duplicates from all the columns
df = df.drop_duplicates()

# use this if you want to remove duplicates only from a subset of columns
df = df.drop_duplicates(subset=list_of_cols)
```

Q25. What is the difference between .loc and .iloc in Pandas?

A25. The loc allows for selection of rows/columns of a Pandas DataFrame by their labels, while .iloc allows for selection of rows/columns of a Pandas DataFame by their integer indices. 