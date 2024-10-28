---

## Pandas DataFrame :
This includes the most commonly used features for data manipulation, analysis, and visualization.

| **Category**                   | **Pandas Function/Method** | **Description**                                               |
|--------------------------------|-----------------------------|---------------------------------------------------------------|
| **Data Structures**            | `DataFrame`                 | Two-dimensional labeled data structure with columns of potentially different types. |
|                                | `Series`                    | One-dimensional labeled array capable of holding any data type. |
| **Creating DataFrames**        | `pd.DataFrame()`            | Creates a DataFrame from various data structures (lists, dicts, etc.). |
|                                | `pd.Series()`               | Creates a Series from a list, array, or dict.                 |
| **Data Input/Output**          | `pd.read_csv()`             | Reads a CSV file into a DataFrame.                            |
|                                | `pd.to_csv()`               | Writes a DataFrame to a CSV file.                             |
|                                | `pd.read_excel()`           | Reads an Excel file into a DataFrame.                         |
|                                | `pd.to_excel()`             | Writes a DataFrame to an Excel file.                          |
|                                | `pd.read_sql()`             | Reads data from a SQL database into a DataFrame.             |
|                                | `pd.read_json()`            | Reads a JSON file into a DataFrame.                           |
|                                | `pd.to_json()`              | Writes a DataFrame to a JSON file.                            |
|                                | `pd.read_hdf()`             | Reads data from an HDF5 file into a DataFrame.               |
|                                | `pd.to_hdf()`               | Writes a DataFrame to an HDF5 file.                           |
| **Data Exploration**           | `df.head()`                 | Returns the first n rows of the DataFrame.                   |
|                                | `df.tail()`                 | Returns the last n rows of the DataFrame.                    |
|                                | `df.info()`                 | Provides a concise summary of the DataFrame.                  |
|                                | `df.describe()`             | Generates descriptive statistics of the DataFrame.            |
|                                | `df.shape`                  | Returns the dimensions (rows, columns) of the DataFrame.     |
|                                | `df.columns`                | Returns the column labels of the DataFrame.                   |
|                                | `df.index`                  | Returns the index labels of the DataFrame.                    |
| **Data Selection**             | `df.loc[]`                  | Accesses a group of rows and columns by labels.               |
|                                | `df.iloc[]`                 | Accesses a group of rows and columns by integer positions.    |
|                                | `df.at[]`                   | Accesses a single value for a row/column label pair.         |
|                                | `df.iat[]`                  | Accesses a single value for a row/column pair by integer position. |
|                                | `df['column_name']`         | Selects a column from the DataFrame.                          |
| **Filtering Data**             | `df[df['column'] > value]` | Filters rows based on column values.                          |
|                                | `df.query()`                | Filters data using a query expression.                        |
|                                | `df.isin()`                 | Filters rows where a column's value is in a list of values.  |
| **Data Manipulation**          | `df.assign()`               | Adds new columns to a DataFrame.                              |
|                                | `df.drop()`                 | Drops specified labels from rows or columns.                  |
|                                | `df.rename()`               | Renames the specified index or columns.                       |
|                                | `df.sort_values()`          | Sorts the DataFrame by the values along either axis.         |
|                                | `df.set_index()`            | Sets the DataFrame index using one or more existing columns.   |
|                                | `df.reset_index()`          | Resets the index of the DataFrame.                            |
|                                | `df.fillna()`               | Fills NA/NaN values with a specified value.                  |
|                                | `df.dropna()`               | Removes missing values from the DataFrame.                   |
|                                | `df.replace()`              | Replaces values in the DataFrame.                             |
| **Aggregation**                | `df.groupby()`              | Groups the DataFrame using a mapper or by a Series of columns. |
|                                | `df.agg()`                  | Applies one or more operations over the specified axis.      |
|                                | `df.mean()`                 | Returns the mean of the values for the requested axis.       |
|                                | `df.sum()`                  | Returns the sum of the values for the requested axis.        |
|                                | `df.min()`                  | Returns the minimum of the values for the requested axis.    |
|                                | `df.max()`                  | Returns the maximum of the values for the requested axis.    |
| **Merging/Joining**           | `pd.merge()`                | Merges two DataFrames based on one or more keys.             |
|                                | `pd.concat()`               | Concatenates two or more DataFrames along a particular axis. |
|                                | `df.join()`                 | Joins columns of another DataFrame to the current DataFrame.  |
| **String Operations**          | `df['column'].str`          | Provides access to string methods for Series.                |
| **Date and Time Functions**    | `pd.to_datetime()`          | Converts a string or integer to datetime.                     |
|                                | `df['date'].dt`             | Provides access to datetime properties.                       |
| **Handling Categorical Data**  | `df['column'].astype('category')` | Converts a column to a categorical data type.         |
|                                | `df['column'].cat.codes`    | Accesses the category codes of a categorical column.         |
| **Visualization**              | `df.plot()`                 | Plots data from the DataFrame.                               |
| **Pivoting and Reshaping**     | `df.pivot()`                | Reshapes the DataFrame based on column values.               |
|                                | `df.pivot_table()`          | Creates a pivot table from the DataFrame.                    |
|                                | `df.melt()`                 | Unpivots a DataFrame from wide format to long format.        |
| **Time Series**                | `pd.date_range()`           | Creates a fixed frequency DateTimeIndex.                     |
|                                | `df.resample()`             | Resamples the time series data.                               |
| **Data Alignment**             | `df.align()`                | Aligns two objects on their axes with the specified join method. |
| **Exporting Data**             | `df.to_json()`              | Exports the DataFrame to a JSON file.                        |
|                                | `df.to_html()`              | Writes the DataFrame to an HTML file.                        |
|                                | `df.to_sql()`               | Writes the DataFrame to a SQL database.                      |
| **Styling DataFrames**         | `df.style`                  | Provides functionality to style DataFrames for better visualization. |
| **Handling Missing Data**      | `df.isnull()`               | Detects missing values in the DataFrame.                     |
|                                | `df.notnull()`              | Detects non-missing values in the DataFrame.                 |
| **Other Functions**            | `pd.concat()`               | Concatenates DataFrames along a particular axis.             |
|                                | `pd.concat()`               | Concatenates DataFrames along a particular axis.             |
|                                | `pd.read_pickle()`          | Reads a pickled DataFrame from a file.                       |
|                                | `df.sample()`               | Returns a random sample of items from the DataFrame.         |

### Conclusion
This table captures a wide range of functionalities provided by the Pandas library. It covers essential methods for data manipulation, analysis, visualization, and more. If you need detailed explanations or examples for any specific function or topic, feel free to ask!


---
---
Here’s a comprehensive guide to commonly used Pandas functions and operations, complete with examples and expected outputs.

### 1. **Creating a DataFrame**
You can create a DataFrame from a dictionary of lists or arrays.

```python
import pandas as pd

data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Los Angeles', 'Chicago']
}

df = pd.DataFrame(data)
print(df)
```
**Output:**
```
      Name  Age         City
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
```

### 2. **Reading CSV Files**
Load data from a CSV file into a DataFrame.

```python
df = pd.read_csv('data.csv')  # Assuming data.csv is in the current directory
print(df.head())
```
**Output:** (Example, actual output will depend on the contents of `data.csv`)
```
   Name  Age         City
0  Alice   25     New York
1    Bob   30  Los Angeles
2  Charlie  35      Chicago
```

### 3. **Writing DataFrame to CSV**
You can write a DataFrame to a CSV file.

```python
df.to_csv('output.csv', index=False)
# Output: A file named 'output.csv' will be created.
```

### 4. **Accessing Columns**
You can access a column by its name.

```python
ages = df['Age']
print(ages)
```
**Output:**
```
0    25
1    30
2    35
Name: Age, dtype: int64
```

### 5. **Accessing Rows**
Use `iloc` or `loc` to access rows.

```python
first_row = df.iloc[0]  # By index
print(first_row)

# OR using loc (by index label)
first_row_label = df.loc[0]
print(first_row_label)
```
**Output:**
```
Name        Alice
Age            25
City     New York
Name: 0, dtype: object
```

### 6. **Filtering Data**
You can filter the DataFrame based on conditions.

```python
filtered_df = df[df['Age'] > 28]
print(filtered_df)
```
**Output:**
```
      Name  Age         City
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
```

### 7. **Adding a New Column**
You can easily add new columns.

```python
df['Country'] = 'USA'
print(df)
```
**Output:**
```
      Name  Age         City Country
0    Alice   25     New York     USA
1      Bob   30  Los Angeles     USA
2  Charlie   35      Chicago     USA
```

### 8. **Renaming Columns**
You can rename columns in a DataFrame.

```python
df.rename(columns={'City': 'Location'}, inplace=True)
print(df)
```
**Output:**
```
      Name  Age    Location Country
0    Alice   25     New York     USA
1      Bob   30  Los Angeles     USA
2  Charlie   35      Chicago     USA
```

### 9. **Dropping Columns**
You can drop columns using the `drop()` method.

```python
df.drop('Country', axis=1, inplace=True)
print(df)
```
**Output:**
```
      Name  Age    Location
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
```

### 10. **Handling Missing Data**
You can check for missing values and fill or drop them.

```python
df['Age'].fillna(df['Age'].mean(), inplace=True)  # Filling missing values
# OR
df.dropna(inplace=True)  # Dropping rows with any missing values
```

### 11. **Group By**
You can group data by one or more columns.

```python
grouped = df.groupby('Location').mean()  # Group by Location and calculate mean of numerical columns
print(grouped)
```
**Output:** (Example, actual output will depend on data)
```
               Age
Location        
Chicago      35.0
Los Angeles  30.0
New York     25.0
```

### 12. **Sorting Data**
Sort the DataFrame by a specific column.

```python
sorted_df = df.sort_values(by='Age', ascending=False)
print(sorted_df)
```
**Output:**
```
      Name  Age    Location
2  Charlie   35      Chicago
1      Bob   30  Los Angeles
0    Alice   25     New York
```

### 13. **Concatenating DataFrames**
You can concatenate two or more DataFrames.

```python
data2 = {
    'Name': ['David', 'Eva'],
    'Age': [40, 22],
    'Location': ['Miami', 'Houston']
}

df2 = pd.DataFrame(data2)
concatenated_df = pd.concat([df, df2])
print(concatenated_df)
```
**Output:**
```
      Name  Age    Location
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
0    David   40        Miami
1      Eva   22      Houston
```

### 14. **Merging DataFrames**
You can merge two DataFrames based on a common column.

```python
data3 = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Salary': [70000, 80000, 60000, 90000]
}

df3 = pd.DataFrame(data3)

merged_df = pd.merge(df, df3, on='Name', how='inner')
print(merged_df)
```
**Output:**
```
      Name  Age    Location  Salary
0    Alice   25     New York   70000
1      Bob   30  Los Angeles   80000
2  Charlie   35      Chicago   60000
```

### 15. **Pivot Table**
You can create a pivot table to summarize data.

```python
pivot = df.pivot_table(values='Age', index='Location', aggfunc='mean')
print(pivot)
```
**Output:** (Example, actual output will depend on data)
```
               Age
Location        
Chicago      35.0
Los Angeles  30.0
New York     25.0
```

### 16. **Descriptive Statistics**
You can get a summary of statistics for numerical columns.

```python
stats = df.describe()
print(stats)
```
**Output:**
```
             Age
count   3.000000
mean   30.000000
std    5.000000
min    25.000000
25%    27.500000
50%    30.000000
75%    32.500000
max    35.000000
```

### 17. **Applying Functions**
You can apply a function to each element or column.

```python
df['Age'] = df['Age'].apply(lambda x: x + 1)  # Increment Age by 1
print(df)
```
**Output:**
```
      Name  Age    Location
0    Alice   26     New York
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 18. **String Methods**
You can use string methods on DataFrame columns.

```python
df['Name'] = df['Name'].str.upper()
print(df)
```
**Output:**
```
      Name  Age    Location
0    ALICE   26     New York
1      BOB   31  Los Angeles
2  CHARLIE   36      Chicago
```

### 19. **Datetime Operations**
Convert a column to datetime and perform date operations.

```python
df['Birthdate'] = pd.to_datetime(['1997-01-01', '1992-02-02', '1987-03-03'])
print(df['Birthdate'].dt.year)  # Extracting the year
```
**Output:**
```
0    1997
1    1992
2    1987
Name: Birthdate, dtype: int64
```

### 20. **Pivoting with `pivot()`**
Create a pivot table with unique index/column pairs.

```python
data4 = {
    'Date': ['2021-01-01', '2021-01-01', '2021-01-02'],
    'City': ['New York', 'Los Angeles', 'New York'],
    'Temperature': [30, 40, 32]
}

df4 = pd.DataFrame(data4)
pivoted_df = df4.pivot(index='Date', columns='City', values='Temperature')
print(pivoted_df)
```
**Output:**
```
City        Los Angeles  New York
Date                             
2021-01-01          40.0      30.0
2021-01-02           NaN      32.0
```

### Summary
Pandas provides a robust set of tools for data manipulation and analysis, allowing for easy handling of

 data from various sources. If you have specific tasks or operations you want to explore further in Pandas, feel free to ask!


---
---
Sure! Let’s continue exploring more advanced Pandas functionalities along with examples and expected outputs.

### 21. **Handling Categorical Data**
You can convert a column to a categorical data type for more efficient memory usage and analysis.

```python
df['City'] = df['City'].astype('category')
print(df['City'].cat.codes)  # Show the codes for the categories
```
**Output:**
```
0    1
1    0
2    2
dtype: int8
```

### 22. **Value Counts**
You can count the occurrences of unique values in a column.

```python
value_counts = df['City'].value_counts()
print(value_counts)
```
**Output:** (Example, actual output will depend on data)
```
Los Angeles    1
Chicago        1
New York       1
Name: City, dtype: int64
```

### 23. **Changing the Index**
You can set one of the columns as the index of the DataFrame.

```python
df.set_index('Name', inplace=True)
print(df)
```
**Output:**
```
         Age         City
Name                     
Alice     26     New York
Bob       31  Los Angeles
Charlie   36      Chicago
```

### 24. **Resetting the Index**
You can reset the index back to the default integer index.

```python
df.reset_index(inplace=True)
print(df)
```
**Output:**
```
      Name  Age         City
0    Alice   26     New York
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 25. **Concatenating along Axis**
You can specify the axis along which to concatenate DataFrames.

```python
df1 = pd.DataFrame({'A': [1, 2], 'B': [3, 4]})
df2 = pd.DataFrame({'A': [5, 6], 'B': [7, 8]})
concatenated_axis0 = pd.concat([df1, df2], axis=0)
print(concatenated_axis0)
```
**Output:**
```
   A  B
0  1  3
1  2  4
0  5  7
1  6  8
```

### 26. **Merging on Multiple Keys**
You can merge DataFrames on multiple keys.

```python
df4 = pd.DataFrame({
    'Name': ['Alice', 'Bob', 'Charlie', 'Alice'],
    'Score': [85, 90, 95, 75],
})

merged_multiple_keys = pd.merge(df, df4, on='Name')
print(merged_multiple_keys)
```
**Output:**
```
      Name  Age         City  Score
0    Alice   26     New York     85
1    Alice   26     New York     75
2      Bob   31  Los Angeles     90
3  Charlie   36      Chicago    NaN
```

### 27. **Using `groupby` with Aggregation Functions**
You can use different aggregation functions on grouped data.

```python
grouped = df.groupby('City').agg({'Age': ['mean', 'max', 'min']})
print(grouped)
```
**Output:** (Example, actual output will depend on data)
```
             Age            
           mean max min
City                     
Chicago      36  36  36
Los Angeles  31  31  31
New York     26  26  26
```

### 28. **Sorting Values by Multiple Columns**
You can sort a DataFrame by multiple columns.

```python
df.sort_values(by=['City', 'Age'], ascending=[True, False], inplace=True)
print(df)
```
**Output:** (Example, actual output will depend on data)
```
      Name  Age         City
0    Alice   26     New York
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 29. **Time Series Analysis**
Pandas can handle time series data with ease. You can convert a column to datetime.

```python
date_data = {
    'Date': pd.date_range(start='2023-01-01', periods=5, freq='D'),
    'Value': [1, 2, 3, 4, 5]
}
ts_df = pd.DataFrame(date_data)
print(ts_df)
```
**Output:**
```
        Date  Value
0 2023-01-01      1
1 2023-01-02      2
2 2023-01-03      3
3 2023-01-04      4
4 2023-01-05      5
```

### 30. **Resampling Time Series Data**
You can resample time series data to different frequencies.

```python
resampled = ts_df.resample('2D', on='Date').sum()
print(resampled)
```
**Output:**
```
            Value
Date             
2023-01-01      1
2023-01-03      5
2023-01-05      5
```

### 31. **Pivoting with `pivot_table()`**
Create a pivot table with aggregation.

```python
pivot_table = df4.pivot_table(index='Name', values='Score', aggfunc='mean')
print(pivot_table)
```
**Output:**
```
          Score
Name           
Alice      80.0
Bob        90.0
Charlie    95.0
```

### 32. **Using `applymap()` for Element-wise Operations**
You can apply a function to each element in the DataFrame.

```python
def square(x):
    return x ** 2

df_numeric = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
squared_df = df_numeric.applymap(square)
print(squared_df)
```
**Output:**
```
   A   B
0  1  16
1  4  25
2  9  36
```

### 33. **Concatenating with `join`**
You can join two DataFrames with different indices.

```python
df5 = pd.DataFrame({'A': [1, 2]}, index=['a', 'b'])
df6 = pd.DataFrame({'B': [3, 4]}, index=['b', 'c'])
joined = df5.join(df6, how='outer')
print(joined)
```
**Output:**
```
     A    B
a  1.0  NaN
b  2.0  3.0
c  NaN  4.0
```

### 34. **Filtering Rows with `query()`**
You can filter rows using the `query()` method.

```python
filtered_query = df.query('Age > 28')
print(filtered_query)
```
**Output:** (Example, actual output will depend on data)
```
      Name  Age         City
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 35. **String Manipulations with `str` accessor**
You can manipulate string data easily.

```python
df['City'] = df['City'].str.lower()
print(df)
```
**Output:**
```
      Name  Age         City
0    Alice   26     new york
1      Bob   31  los angeles
2  Charlie   36      chicago
```

### 36. **Creating Dummy Variables**
You can convert categorical variables into dummy/indicator variables.

```python
dummies = pd.get_dummies(df['City'])
print(dummies)
```
**Output:**
```
   chicago  los angeles  new york
0       0            0         1
1       0            1         0
2       1            0         0
```

### 37. **Using `fillna()` for Imputation**
You can replace NaN values with a specific value.

```python
df.fillna({'Age': df['Age'].mean()}, inplace=True)
print(df)
```
**Output:** (Example, actual output will depend on data)
```
      Name  Age         City
0    Alice   26     New York
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 38. **Cross-Tabulation**
You can create a cross-tabulation of two (or more) factors.

```python
cross_tab = pd.crosstab(df['City'], df['Age'])
print(cross_tab)
```
**Output:** (Example, actual output will depend on data)
```
Age         26  31  36
City                  
chicago      0   0   1
los angeles   0   1   0
new york     1   0   0
```

### 39. **Using `style` for Formatting**
You can style your DataFrame for better visual representation.

```python
styled_df = df.style.highlight_max(axis=0)
styled_df  # In Jupyter Notebooks, this will render the styled DataFrame
```

### 40. **Exporting to Excel**
You can export your DataFrame to an Excel file.

```python
df.to_excel('output.xlsx', index=False)
# Output:

 A file named 'output.xlsx' will be created.
```

### Conclusion

Pandas is a powerful library for data manipulation and analysis, offering a plethora of functions to handle various data operations effectively. The above examples illustrate just a subset of its capabilities. If you have specific scenarios or additional topics you'd like to delve into, feel free to ask!

---
---

Absolutely! Let's delve into even more advanced Pandas functionalities, covering additional techniques for data manipulation, visualization, and more nuanced operations.

### 41. **Iterating Over Rows**
You can iterate over the rows of a DataFrame using `iterrows()`.

```python
for index, row in df.iterrows():
    print(f"Index: {index}, Name: {row['Name']}, Age: {row['Age']}, City: {row['City']}")
```
**Output:**
```
Index: 0, Name: Alice, Age: 26, City: new york
Index: 1, Name: Bob, Age: 31, City: los angeles
Index: 2, Name: Charlie, Age: 36, City: chicago
```

### 42. **Using `iloc` for Slicing**
You can use `iloc` for slicing the DataFrame by row and column indices.

```python
sliced_df = df.iloc[0:2, 0:2]  # Slicing first two rows and first two columns
print(sliced_df)
```
**Output:**
```
      Name  Age
0    Alice   26
1      Bob   31
```

### 43. **Using `loc` for Label-Based Indexing**
You can use `loc` to filter rows based on label names.

```python
selected = df.loc[df['Age'] > 28, ['Name', 'City']]
print(selected)
```
**Output:**
```
      Name         City
1      Bob  los angeles
2  Charlie      chicago
```

### 44. **Transforming Data with `transform()`**
You can use the `transform()` method to perform operations that return an object that is indexed the same as the original DataFrame.

```python
df['Age_transformed'] = df['Age'].transform(lambda x: x + 10)
print(df)
```
**Output:**
```
      Name  Age         City  Age_transformed
0    Alice   26     new york               36
1      Bob   31  los angeles               41
2  Charlie   36      chicago               46
```

### 45. **Using `apply()` for Custom Functions**
You can apply a custom function to rows or columns using `apply()`.

```python
def categorize_age(age):
    if age < 30:
        return 'Young'
    else:
        return 'Adult'

df['Age_Category'] = df['Age'].apply(categorize_age)
print(df)
```
**Output:**
```
      Name  Age         City Age_Category
0    Alice   26     new york         Young
1      Bob   31  los angeles        Adult
2  Charlie   36      chicago        Adult
```

### 46. **Using `drop_duplicates()`**
You can drop duplicate rows based on one or more columns.

```python
df_with_duplicates = df.append(df.iloc[0])  # Adding a duplicate for demonstration
df_no_duplicates = df_with_duplicates.drop_duplicates()
print(df_no_duplicates)
```
**Output:**
```
      Name  Age         City Age_Category
0    Alice   26     new york         Young
1      Bob   31  los angeles        Adult
2  Charlie   36      chicago        Adult
```

### 47. **Changing Data Types with `astype()`**
You can change the data type of a column.

```python
df['Age'] = df['Age'].astype(float)
print(df.dtypes)
```
**Output:**
```
Name            object
Age           float64
City           object
Age_Category   object
dtype: object
```

### 48. **Using `isin()` for Filtering**
You can filter rows based on whether a column's value is in a list of values.

```python
cities_to_filter = ['new york', 'chicago']
filtered_cities = df[df['City'].isin(cities_to_filter)]
print(filtered_cities)
```
**Output:**
```
      Name  Age     City Age_Category
0    Alice   26 new york         Young
2  Charlie   36  chicago        Adult
```

### 49. **Handling Outliers with `clip()`**
You can clip values in a DataFrame to limit the range of values.

```python
df['Age_clipped'] = df['Age'].clip(lower=28, upper=35)
print(df[['Age', 'Age_clipped']])
```
**Output:**
```
   Age  Age_clipped
0   26          28
1   31          31
2   36          35
```

### 50. **Creating a DataFrame from a List of Dictionaries**
You can create a DataFrame from a list of dictionaries directly.

```python
data_list = [
    {'Name': 'Alice', 'Age': 26, 'City': 'New York'},
    {'Name': 'Bob', 'Age': 31, 'City': 'Los Angeles'},
    {'Name': 'Charlie', 'Age': 36, 'City': 'Chicago'},
]

df_from_list = pd.DataFrame(data_list)
print(df_from_list)
```
**Output:**
```
      Name  Age         City
0    Alice   26     New York
1      Bob   31  Los Angeles
2  Charlie   36      Chicago
```

### 51. **Setting Display Options**
You can set display options to control the output format.

```python
pd.set_option('display.max_rows', 10)  # Set the maximum rows to display
pd.set_option('display.max_columns', 5)  # Set the maximum columns to display
```

### 52. **Using `pivot()` for Reshaping Data**
You can reshape the DataFrame using `pivot()`.

```python
data = {
    'Date': ['2023-01-01', '2023-01-01', '2023-01-02'],
    'City': ['New York', 'Los Angeles', 'New York'],
    'Temperature': [30, 40, 32],
}

df_reshape = pd.DataFrame(data)
pivoted = df_reshape.pivot(index='Date', columns='City', values='Temperature')
print(pivoted)
```
**Output:**
```
City        Los Angeles  New York
Date                             
2023-01-01          40.0      30.0
2023-01-02           NaN      32.0
```

### 53. **Using `pipe()` for Method Chaining**
You can use `pipe()` to apply a function while maintaining method chaining.

```python
def add_10(df):
    df['Age'] += 10
    return df

new_df = df.pipe(add_10)
print(new_df)
```
**Output:**
```
      Name  Age         City Age_Category
0    Alice   36     new york         Young
1      Bob   41  los angeles        Adult
2  Charlie   46      chicago        Adult
```

### 54. **Visualizing Data with Matplotlib and Pandas**
You can create visualizations directly from a DataFrame.

```python
import matplotlib.pyplot as plt

df['Age'].plot(kind='bar', title='Age of Individuals')
plt.xlabel('Name')
plt.ylabel('Age')
plt.xticks(ticks=range(len(df)), labels=df['Name'], rotation=0)
plt.show()
```
**Output:** 
A bar chart showing the age of individuals.

### 55. **Using `style.format()` for Data Formatting**
You can format the output display of DataFrames.

```python
styled_df = df.style.format({'Age': '{:.1f}', 'City': lambda x: x.title()})
styled_df  # Rendered in Jupyter Notebooks
```

### 56. **Using `numpy` with Pandas**
You can use NumPy functions within Pandas operations.

```python
import numpy as np

df['Age'] = np.where(df['Age'] < 30, 'Young', 'Adult')
print(df)
```
**Output:**
```
      Name     Age         City
0    Alice   Young     new york
1      Bob   Adult  los angeles
2  Charlie   Adult      chicago
```

### 57. **Using `pd.Series` for Specialized Operations**
You can create a Pandas Series for specialized operations.

```python
age_series = pd.Series([26, 31, 36])
mean_age = age_series.mean()
print(mean_age)
```
**Output:**
```
31.0
```

### 58. **Using Regular Expressions for String Operations**
You can use regex to filter string columns.

```python
df_filtered = df[df['City'].str.contains('new', case=False, regex=True)]
print(df_filtered)
```
**Output:**
```
      Name  Age     City Age_Category
0    Alice   26 new york         Young
```

### 59. **Saving and Loading DataFrame with HDF5**
You can save DataFrames in HDF5 format for fast I/O operations.

```python
df.to_hdf('data.h5', key='df', mode='w')
loaded_df = pd.read_hdf('data.h5', 'df')
print(loaded_df)
```
**Output:**
```
      Name  Age         City Age_Category
0    Alice   26     new york         Young
1      Bob   31  los angeles        Adult
2  Charlie   36      chicago        Adult
```

### 60. **Using `pd.cut()` for

 Binning Data**
You can bin continuous data into discrete intervals.

```python
bins = [20, 30, 40, 50]
labels = ['20-30', '30-40', '40-50']
df['Age_Bin'] = pd.cut(df['Age'], bins=bins, labels=labels)
print(df[['Name', 'Age', 'Age_Bin']])
```
**Output:** (Example, actual output will depend on data)
```
      Name  Age Age_Bin
0    Alice   26   20-30
1      Bob   31   30-40
2  Charlie   36   30-40
```

### Conclusion
These additional functionalities further showcase the versatility and power of Pandas for data analysis and manipulation. Whether it’s advanced filtering, reshaping, or visualizing data, Pandas offers tools to streamline these tasks effectively. If you have any more specific topics or functions in mind, feel free to ask!

---
---


---
---




