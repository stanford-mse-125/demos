# Functions - Reference Guide 

This is a list of some useful functions used in the lecture demos. In most cases we link the official documentation so you may refer to it to learn about the arguments and usage.

## Exploratory Data Analysis

### Base python functions

* type() : Returns class type of the object passed as parameter 

### Pandas functions

* .head() : This function returns the first n rows for the object based on position. It is useful for quickly testing if your object has the right type of data in it.
  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html


* .describe(): Useful for numerical data. Generates descriptive statistics including those that summarize the central tendency, dispersion and shape of a dataset’s distribution, excluding `NaN` values.    
  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html


* .isnull() : This function takes a scalar or array-like object and indicates whether values are missing (`NaN` in numeric arrays, `None` or `NaN` in object arrays, `NaT` in datetimelike). Returns `True` or `False` values.  
   **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.isnull.html
   
 
* .is_unique : Return boolean (True/False) if values in the object are unique.  
    **Documentation** :https://pandas.pydata.org/docs/reference/api/pandas.Series.is_unique.html

 
* .any() : Return whether any element is True, potentially over an axis. Returns False unless there is at least one element within a series or along a Dataframe axis that is True or equivalent (e.g. non-zero or non-empty).    
    **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.any.html


* read_csv() : Read a comma-separated values (csv) file into DataFrame.  
  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html


* .apply() : Apply a function along an axis of the DataFrame. This can be used in conjunction with a lambda function as seen in the class demo.   
  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.apply.html
  
  
* .value_counts() : Return a Series containing counts of unique values.   
   **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html
   
   
* .to_datetime() : Convert argument to datetime.  
   **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.to_datetime.html

* .drop_duplicates() : Return DataFrame with duplicate rows removed. Use `subset` argument to specify which column to de-dupe by.
   **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop_duplicates.html
  
* .merge() : Merge DataFrame or named Series objects with a database-style join. Allows you to perform inner, left, right, or outer joins. Some intuition behind joins from [Discussion 2](https://colab.research.google.com/github/stanford-mse-125/section/blob/main/Discussions/Discussion_2.ipynb) might be helpful. 
   **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html 
   
#### Pandas Subsetting

Often you'll want to look at not an entire dataframe, but some subset of the dataframe. It is very easy to subset your data using Pandas. There are a few ways to subset data in Pandas:

- Direct row subset: when you only want to subset the rows in the dataframe (but keep all the columns), you can directly subset using the syntax `df[row_selector]`, where `row_selector` is a list-like object (Python list, 1D NumPy ndarray, Pandas Series) indicating which rows to keep, using either booleans or indices.
    * df[b] a boolean vector b of length n to select rows
    
    
- Direct col subset: similarly if you only want to subset your columns (but keep all rows), then you can do `df[col_selector]` where `col_selector` indicates which columns should be kept. The `col_selector` here can be names of columns, indices, or booleans.
    * df['foo'] a column name 'foo' to select one column
    * df[['foo','bar']] a list of column names to select several columns
    
    
- Using `.loc`: if you want to subset both rows and columns, then you should subset using the syntax `df.loc[row_selector, col_selector]`. It's worth noting that you can do only row or column selection using `df.loc` if you put `:` in place of the selector that you don't need to use. 
You can query df.loc with
    * df.loc['foo'] a column name 'foo' to select one column
    * df.loc['foo','bar'] a list of column names to select several columns

  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html


- Using `.iloc`: similar to `.loc`, but for when you want to subset your rows and/or columns using *indices* instead of names or booleans. You can query df.iloc with
    * df.iloc[l] to select the rows with indices in the list l
    * df.iloc[:, l] to select the columns with indices in the list l
  
  **Documentation** : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iloc.html
  
 ### Seaborn plotting functions
 
* sns.histplot : Plot univariate or bivariate histograms to show distributions of datasets.   
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.histplot.html


* sns.countplot : Show the counts of observations in each categorical bin using bars. A count plot can be thought of as a histogram across a categorical, instead of quantitative, variable.  
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.countplot.html
      
   
* sns.lineplot : Draw a lineplot.  
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.lineplot.html
   
   
* sns.scatterplot : Draw a scatter plot.  
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.scatterplot.html
   
   
* sns.boxplot : Draw a box plot to show distributions with respect to categories.  
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.boxplot.html
   
   
* sns.barplot : A bar plot represents an estimate of central tendency for a numeric variable with the height of each rectangle and provides some indication of the uncertainty around that estimate using error bars.   
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.barplot.html 
   
   
* sns.catplot : This function provides access to several axes-level functions that show the relationship between a numerical and one or more categorical variables using one of several visual representations. The kind parameter selects the underlying axes-level function to use. This function allows you to plot boxplots, violin plots, and so on.   
  **Documentation** : https://seaborn.pydata.org/generated/seaborn.catplot.html
   
 

 