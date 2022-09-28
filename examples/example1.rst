Examples
===============

.. toctree::
    :hidden:
    :maxdepth: 100
   
   

   	Uploading files to Snowflake <self>
    example2

.. raw:: html
	
	<h2>Uploading CSV File to Snowflake database and reading it</h2>

In this example, we show you how to upload a ``.csv`` file to your Snowflake account and read it using ``read_csv()`` method. 


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

**Step 2:** Upload the ``test.csv`` file to your Snowflake account

.. code-block:: python

	t = ponder.utils.core.Teleporter()
	t.depulso("test.csv")


**Step 3:** Read your ``test.csv`` file

.. code-block:: python

	df = pd.read_csv(t.teleported_path("test.csv"), header=0)
	df.head()