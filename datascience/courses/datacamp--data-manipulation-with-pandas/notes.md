# Notes on Data Science Courses

## Data Manipulation with `pandas`
Link to course: [here](https://learn.datacamp.com/courses/data-manipulation-with-pandas)

#### Transforming Data

* A DataFrame (DF) has a tabular structure. In other words, it can be understood to feature indexed _rows_ and _columns_.
* DataFrames can be created with `pd.DataFrame()`. The method takes a list of dictionaries or a dictionary of lists as an argument by which the DataFrame is constructed.
  * e.g. `{
  "date": ["2019-11-17", "2019-12-01"],
  "small_sold": [10859987,9291631],
  "large_sold": [7674135,6238096]
}` for a dictionary of list.
* You can construct a DataFrame from an external file with the `pd.read_csv(path)` method. To write to an external file, use the `.to_csv(path)` method on the DataFrame.
* A DataFrame can be inspected with its `.describe()`, `.head()` and `.tail()` methods.
* The `sort_values()` method takes a string or array of strings respective to the column name(s) by which the DF shall be sorted. 
  * Descending/Ascending order in sorting can be controlled with the Boolean `ascending` argument of `sort_values`.
* A DataFrame can be _subset_. A DataFrame of all rows limited to the column `column1` can be subset with `only_column1 = df[df["column1"]]`
* A new column to a DF can added with `df["New Column"] = value`.
  
#### Aggregating Data

* The _mean_ and _median_ of a DataFrame column can be determined with the `.mean()` and `.median()` method (e.g. `df.mean()`)
* Other descriptive statistics as the _max_, _min_ or _cumsum_ (cumulative sum) are available to their respective equally named methods.
* Values can be counted in their number or in proportion with the `.value_counts()` method. To determine by proportion, use the Boolean `normalize` argument. 
  * Counted values can also be sorted with the Boolean `sort` attribute.
* We can group entries in a DataFrame with the `.groupby()` method. The method takes a string or array of strings of the respective column name(s) by which the data should be grouped.
  * e.g. `sales.groupby("type")["weekly_sales"].sum()`
* The `.agg()` method allows to aggregate computations of statistical functions on (multiple) columns. `NumPy` features a lot of statistical functions that can be used here.
  * e.g. `sales.groupby("type")["weekly_sales"].agg([np.min,np.max])`
* Aggregating data into spreadsheets is achieved with the `.pivot_table()` method.
  
#### Slicing and Indexing

* Columns can be indexed.
* A DataFrame can feature multiple indexes at once. We speak of index _levels_. The outer index is level 0, following inner indexes with level 1, level 2... 
* To set an index, use `.set_index()` with a string or array of strings of the respective columns that shall serve as an index.
* An index can be reset with `.reset_index()`
* To subset by index, use the `.loc[]` method. Emphasis on the square brackets!
* To subet by index level, use the `iloc[]` method.
* `.loc[]` can take a single argument to subset by index.
* `.loc[]` can also take a tuple `()` as an argument to subset by multi-level indexes. 
  * e.g. `temperatures.loc[[("Brazil", "Rio De Janeiro")]]` will subset for the outer index level _country_ (Brazil) and the inner level _city_ (Rio de Janeiro)
*  The tuple for `.loc[]` can also feature multiple subsettings.
   *    * e.g. `temperatures.loc[[("Brazil", "Rio De Janeiro"), ("Germany", "Berlin")]]`
* To sort by index, use `.sort_index()`. The Boolean `ascending` argument is available.
* Slicing with `.loc[]` can be achieved with the common `from:to` slicing pattern.
  * e.g. `countries.loc["Germany":"Russia"]`.
* To slice by multi-level indexes, provide tuples.
  * e.g. `countries.loc[("Pakistan","Lahore"):("Russia","Moscow")]`
* DataFrames can also be sliced in both directions (rows _and_ columns). Provide a second argument to the `.loc[]` method to achieve slicing by column.
  * e.g. `countries.loc["India":"Iraq", "column1":"column2"]`
* The same behaviour for multi-level indexes applies to the two-dimensional slicing. (see above).
* DataFrames can be sliced conditionally, i.e. a column value has to pass the condition to be included. 
    * e.g. `country[country["is_eu_member"] == True]`
* To slice by a `Date` value, use the full date in ISO 8601 format (`yyyy-mm-dd`).
  * e.g. `temperatures[(temperatures["date"] >= "2010-01-01") & (temperatures["date"] <= "2011-12-31")]`
* DataFrames can be plotted with the power of `matplotlib` with the `.plot()` method. The various types of plots can be defined with the `type` argument. 
  * A simple histogram can be plotted with `.hist()`.
* Missing values in a row or column (or total DF) can be identified with `isna()` and further scanned over the entire category with the following `.any()` method.
  * e.g. `avocades.isna().any()` will look for any missing values in the rows or columns of the _avocados_ DataFrame.
* Missing values can be removed with `.dropna()`
