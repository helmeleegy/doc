Reading existing tables on Snowflake
===============

.. toctree::
	:hidden:
	:maxdepth: 100


In this example, we show you how to read an exsiting table that on your Snowflake database using ``read_sql()`` method. Assume you have previously created a table called ``TEST`` in your database. 


**Step 1:** Connect to your Snowflake database and initialize the connection

.. code-block:: python

	import modin.pandas as pd
	import ponder.snowflake
	from ponder.utils.core import Teleporter

	# Create a Ponder Snowflake Connections object
	snowflake_con = ponder.snowflake.connect(
	    user="BAHADORSAKET",
	    password="PONDER2020",
	    account="RQ08674.us-east-2.aws",
	    role="ACCOUNTADMIN",
	    database="TEST",
	    schema="PUBLIC",
	    warehouse="COMPUTE_WH",
	)

	# Initialize the Snowflake connection
	ponder.snowflake.init(snowflake_con, timeout=1200)

**Step 2:** Read the ``TEST`` table that you have already created in your database.

.. code-block:: python

	df= pd.read_sql("TEST", "auto")
	df.head()