pandas Utilities supported
=================================
.. toctree::
    :hidden:
    :maxdepth: 100
   

The following table lists both implemented and not implemented methods. If you have need
of an operation that is listed as not implemented, feel free to open email us at 
support@ponder.io.

The following table is structured as follows: The first column contains the method name.
The second column contains link to a description of corresponding pandas method.
The third column is a flag for whether or not there is an implementation in Modin for
the method in the left column. ``Y`` stands for yes, ``N`` stands for no, ``P`` stands
for partial (meaning some parameters may not be supported yet), and ``D`` stands for
default to pandas.


**Utility**

+---------------------------+---------------------------------+----------------------------------------------------+
| Utility method            | Ponder Implementation? (Y/N/P/D)| Notes for Current implementation                   |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.concat`_              | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.eval`_                | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.unique`_              | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| ``pd.value_counts``       | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.cut`_                 | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.to_numeric`_          | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.factorize`_           | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.qcut`_                | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| ``pd.match``              | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.to_datetime`_         | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.get_dummies`_         | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.date_range`_          | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.bdate_range`_         | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| `pd.to_timedelta`_        | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| ``pd.options``            | N                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+
| ``pd.datetime``           | D                               |                                                    |
+---------------------------+---------------------------------+----------------------------------------------------+


.. _`pd.concat`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.concat.html#pandas.concat
.. _`pd.eval`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.eval.html#pandas.eval
.. _`pd.unique`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.unique.html#pandas.unique
.. _`pd.cut`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.cut.html#pandas.cut
.. _`pd.to_numeric`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_numeric.html#pandas.to_numeric
.. _`pd.factorize`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.factorize.html#pandas.factorize
.. _`pd.qcut`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.qcut.html#pandas.qcut
.. _`pd.to_datetime`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html#pandas.to_datetime
.. _`pd.get_dummies`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.get_dummies.html#pandas.get_dummies
.. _`pd.date_range`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html#pandas.date_range
.. _`pd.bdate_range`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.bdate_range.html#pandas.bdate_range
.. _`pd.to_timedelta`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_timedelta.html#pandas.to_timedelta