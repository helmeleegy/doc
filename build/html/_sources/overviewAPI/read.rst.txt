pd.read_<file> and I/O APIs
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


**Read**

+--------------------+---------------------------------+----------------------------------------------------+
| IO method          | Ponder Implementation? (Y/N/P/D)| Notes for Current implementation                   |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_csv`_        | Y                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_table`_      | Y                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_parquet`_    | N                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_json`_       | P                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_html`_       | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_clipboard`_  | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_excel`_      | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_hdf`_        | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_feather`_    | N                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_msgpack`_    | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_stata`_      | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_sas`_        | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_pickle`_     | D                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+
| `read_sql`_        | Y                               |                                                    |
+--------------------+---------------------------------+----------------------------------------------------+

.. _`read_csv`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html#pandas.read_csv
.. _`read_table`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_table.html#pandas.read_table
.. _`read_parquet`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_parquet.html#pandas.read_parquet
.. _`read_json`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_json.html#pandas.read_json
.. _`read_html`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_html.html#pandas.read_html
.. _`read_clipboard`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_clipboard.html#pandas.read_clipboard
.. _`read_excel`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html#pandas.read_excel
.. _`read_hdf`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_hdf.html#pandas.read_hdf
.. _`read_feather`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_feather.html#pandas.read_feather
.. _`read_msgpack`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_msgpack.html#pandas.read_msgpack
.. _`read_stata`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_stata.html#pandas.read_stata
.. _`read_sas`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_sas.html#pandas.read_sas
.. _`read_pickle`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_pickle.html#pandas.read_pickle
.. _`read_sql`: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_sql.html#pandas.read_sql