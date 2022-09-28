Supported APIs
===============

.. note:: 
  | *Estimated Reading Time: 10 minutes*
  | You can follow along this tutorial in a Jupyter notebook `here <https://github.com/modin-project/modin/tree/master/examples/quickstart.ipynb>`_. 


.. toctree::
    :hidden:
    :maxdepth: 100
   


Attributes and underlying data
------------


.. dropdown:: DataFrame.select_dtypes()

	Return a subset of the DataFrame’s columns based on the column dtypes.

	This returns a Series with the data type of each column. The result’s index is the original DataFrame’s columns. Columns with mixed types are stored with the object dtype. See the User Guide for more.

	**Returns : pandas.Series**
	The data type of each column.

	.. code-block::
	>>> df = pd.DataFrame({'float': [1.0],'int': [1],'datetime': [pd.Timestamp('20180310')],'string': ['foo']})
	>>> df.dtypes
	float              float64
	int                  int64
	datetime    datetime64[ns]
	string              object
	dtype: object

Combining / Joining / Merging
------------

.. dropdown:: DataFrame.append()
	
	Append rows of other to the end of caller, returning a new object.

.. dropdown:: concat()

	Concatenate pandas objects along a particular axis with optional set logic along the other axes.

.. dropdown:: DataFrame.merge()

	Merge DataFrame objects with a database-style join.

.. dropdown:: DataFrame.insert()

	Insert column into DataFrame at specified location.

.. dropdown:: DataFrame.join()

	Join columns of another DataFrame.

.. dropdown:: DataFrame.assign()

	Assign new columns to a DataFrame.



Indexing / Iteration
------------

.. dropdown:: DataFrame.head()

	Return the first n rows.

.. dropdown:: DataFrame.loc

	Access a group of rows and columns by label(s) or a boolean Series.

.. dropdown:: DataFrame.iloc

	Purely integer-location based indexing for selection by position.

.. dropdown:: DataFrame.get()

	Get item from object for given key (DataFrame column, Panel slice, etc.).

.. dropdown:: DataFrame.keys()

	Return alias for columns.

.. dropdown:: DataFrame.items()

	This is an alias of iteritems

.. dropdown:: DataFrame.tail()

	Return the last n rows.

.. dropdown:: Series.str.contains()


.. dropdown:: DataFrame.query()

	Query the columns of a DataFrame with a boolean expression.

.. dropdown:: DataFrame.pop()
	
	Return item and drop from frame.


.. dropdown:: DataFrame.at

	Access a single value for a row/column label pair.

.. dropdown:: DataFrame.idxmax()

	Return index of first occurrence of maximum over requested axis.

.. dropdown:: DataFrame.idxmin()

	Return index of first occurrence of minimum over requested axis.

.. dropdown:: DataFrame.iat

	Access a single value for a row/column pair by integer position.


Read / Write
------------


.. dropdown:: read_csv()


.. dropdown:: DataFrame.read_table()


.. dropdown:: pandas.read_sql()


.. dropdown:: read_sql_query()


.. dropdown:: read_sql_table



Reindexing / Selection / Label Manipulation
------------


.. dropdown:: DataFrame.drop ()

	Drop specified labels from columns.

.. dropdown:: DataFrame.reset_index()
	
	Reset the index, or a level of it.


.. dropdown:: DataFrame.rename()

	Alter axes labels

.. dropdown:: DataFrame.set_index()

	Set the DataFrame index (row labels) using one or more existing columns.

.. dropdown:: DataFrame.sample()

	Return a random sample of items from an axis of object.

.. dropdown:: DataFrame.take()

	Return the elements in the given positional indices along an axis.

.. dropdown:: DataFrame.add_prefix()

	Prefix labels with string prefix.

.. dropdown:: DataFrame.add_suffix()
	
	Suffix labels with string suffix.



.. dropdown:: read_sql_table





Computations / Descriptive Stats
------------

.. dropdown:: DataFrame.mean()

	Return the mean of the values.

.. dropdown:: DataFrame.sum()

	Return the sum of the values.

.. dropdown:: DataFrame.describe()

	Generate descriptive statistics that summarize the central tendency, dispersion and shape of a dataset’s distribution, excluding NaN values.

.. dropdown:: DataFrame.count()

	Count non-NA cells for each column.

.. dropdown:: DataFrame.max()

	Return the maximum of the values.

.. dropdown:: DataFrame.std()

	Return sample standard deviation.

.. dropdown:: DataFrame.min()

	Return the minimum of the values.

.. dropdown:: DataFrame.median()

	Return the median of the values for the requested axis.

.. dropdown:: DataFrame.any()

	Return whether any element is True.

.. dropdown:: DataFrame.cumsum()

	Return cumulative sum over a DataFrame or Series axis.

.. dropdown:: DataFrame.quantile()
	
	Return value at the given quantile.

.. dropdown:: DataFrame.all()

	Return whether all elements are True.

.. dropdown:: DataFrame.mode()

.. dropdown:: DataFrame.product()

	Return the product of the values.

.. dropdown:: DataFrame.prod()

	Return the product of the values.

.. dropdown:: DataFrame.cummin()

	Return cumulative minimum over a DataFrame or Series axis.

.. dropdown:: DataFrame.cummax()

	Return cumulative maximum over a DataFrame or Series axis.



Function application GroupBy & Window
------------

.. dropdown:: DataFrame.groupby()

	Group DataFrame or Series using a Series of columns.



Reshaping / Sorting / Transposing
------------

.. dropdown:: DataFrame.sort_values()

	Sort by the values along either axis.


.. dropdown:: DataFrame.sort_index()

	Sort object by labels (along an axis)


.. dropdown:: DataFrame.pivot()
	
	Return reshaped DataFrame organized by given index / column values.


.. dropdown:: DataFrame.squeeze()

	Squeeze 1 dimensional axis objects into scalars.




Binary operator functions
------------

.. dropdown:: DataFrame.add()

	Get Addition of dataframe and other, element-wise (binary operator +).


.. dropdown:: DataFrame.subtract()

	Get Subtraction of dataframe and other, element-wise (binary operator -).
	

.. dropdown:: DataFrame.multiply()

	Get Multiplication of dataframe and other, element-wise (binary operator mul).


.. dropdown:: DataFrame.divide()

	Get Floating division of dataframe and other, element-wise (binary operator truediv).


.. dropdown:: DataFrame.eq()
	
	Get Equal to of dataframe and other, element-wise (binary operator eq).


.. dropdown:: DataFrame.lt()

	Get Less than of dataframe and other, element-wise (binary operator lt).

.. dropdown:: DataFrame.ne()
	
	Compare if the current value is not equal to the other.


.. dropdown:: DataFrame.truediv()

	Get Floating division of dataframe and other, element-wise (binary operator /).


.. dropdown:: DataFrame.mod()

	Get Modulo of dataframe and other, element-wise (binary operator %).


.. dropdown:: DataFrame.ge()

	Compare if the current value is greater than or equal to the other.


.. dropdown:: DataFrame.floordiv()

	Get Integer division of dataframe and other, element-wise (binary operator //).


.. dropdown:: DataFrame.le()

	Compare if the current value is less than or equal to the other.


.. dropdown:: DataFrame.rsub()

	Get Subtraction of dataframe and other, element-wise (binary operator -).


.. dropdown:: DataFrame.radd()

	Get Addition of dataframe and other, element-wise (binary operator +).


.. dropdown:: DataFrame.rmul()

	Get Multiplication of dataframe and other, element-wise (binary operator *).





Missing Data handling
------------

.. dropdown:: DataFrame.dropna()

	Remove missing values.


.. dropdown:: DataFrame.fillna()
	
	Fill NA/NaN values.


.. dropdown:: DataFrame.bfill()

	Synonym for DataFrame.fillna() or Series.fillna() with method=`bfill`



Conversion
------------

.. dropdown:: DataFrame.isnull()

	Detects missing values for items in the current Dataframe.


.. dropdown:: DataFrame.copy()
	
	Make a copy of this object’s indices and data.


.. dropdown:: DataFrame.notnull()

	Detects non-missing values for items in the current Dataframe.


.. dropdown:: DataFrame.isna()

	Detects missing values for items in the current Dataframe.




Serialization / IO / Conversion
------------

.. dropdown:: DataFrame.to_sql()


.. dropdown:: Series.to_frame()
