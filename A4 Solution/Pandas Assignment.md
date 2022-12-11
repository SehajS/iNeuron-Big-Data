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

Q4. How do you rename columns in a Pandas DataFrame?

A4. 

Q5. How do you drop columns in a Pandas DataFrame?

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

Q9. How do you concatenate two Pandas DataFrames?

A9. One can concat two Pandas DataFrames using `pd.concat()` function as shown below:

```{python}

```

Q10. How do you merge two Pandas DataFrames on a specific column?

A10. Depending upon the type of join one would like to perform (by default, it is inner join), two dataframes `df1` and `df2` can be merged on the column `col_name` using the following syntax:

```{python}
df = pd.merge(df1, df2, on='col_name', how='inner')
```

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?

A11. 

Q12. How do you pivot a Pandas DataFrame?

Q13. How do you change the data type of a column in a Pandas DataFrame?

Q14. How do you sort a Pandas DataFrame by a specific column?

Q15. How do you create a copy of a Pandas DataFrame?

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?

Q17. How do you calculate the mean of a column in a Pandas DataFrame?

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?

Q20. How do you select specific columns in a DataFrame using their labels?

Q21. How do you select specific rows in a DataFrame using their indexes?

Q22. How do you sort a DataFrame by a specific column?

Q23. How do you create a new column in a DataFrame based on the values of another column?

Q24. How do you remove duplicates from a DataFrame?

Q25. What is the difference between .loc and .iloc in Pandas?