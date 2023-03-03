# intro

# eda

sales.ipynb
* .head()
* .describe()
* .isnull()
* .any()
* read_csv
* .plot(kind='bar')
* .value_counts()
* .hist()
* .apply(lambda x: ...)
* .sort_values()
* query df with 
    * df[b] a boolean vector b of length n to select rows
    * df['foo'] a column name 'foo' to select one column
    * df[['foo','bar']] a list of column names to select several columns
* query df.iloc with
    * df.iloc[l] to select the rows with indices in the list l
    * df.iloc[:, l] to select the columns with indices in the list l
* sns.histplot, countplot, catplot, lineplot, scatterplot, barplot

# sqlish

fires.ipynb
* dropna
* drop_duplicates
* sns.facet
* sns.boxplot
* merge (not join, oddly enough)

consider
* melt 
    * eg to turn a comparison table into long format for easier plotting
* pivot
    * take long-form dataset and put all data for each (eg) patient into one row