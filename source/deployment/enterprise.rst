Ponder Cloud - Local Machine 
==============================


.. toctree::
    :hidden:
    :maxdepth: 100
 


.. raw:: html

	In this guide you will:
	<ol>
		<li>Sign up for Ponder Account</li>
		<li>Create Snowflake Account (if you haven’t already)</li>
		<li>Download and Run the wheel file </li>
		<li>Connect to your DB and start Pondering 🎉</li>
	</ol>

.. raw:: html

	<h2>Step 1: Sign up for Ponder Account</h2>


If you haven’t already, please go to `Ponder's product page <https://ponder.io/>`_ and sign up for Ponder using your email address.

.. raw:: html

	<h2>Step 2: Create Snowflake Account (if you haven’t already)</h2>


If you have a snowflake account you can skip this step. Otherwise, you first need to create a snowflake account. Follow our :doc:`step-by-step guide</resources/SnowflakeAccountCreation>` on how to create an account on Snowflake. 

.. raw:: html

	<h2>Step 3: Download and Run the wheel file</h2>

First download the wheel file from `here <s3://assets-ponder/ponder-lib/ponder-0.0.1-py3-none-any.whl>`_ .

Open the ``terminal`` and go to the directory where you downloaded the wheel file. You then need to pip install the wheel using the following command.

.. code-block:: bash

	pip install ponder-0.0.1-py3-none-any.whl --force-reinstall ()


.. raw:: html

	<h2>Step 4: Open ``iPython``</h2>
Now, open a ipython terminal using the following command in your terminal


.. code-block:: bash

	iPython


.. raw:: html

	<h2>Step 5: Connect to your DB and start Pondering 🎉</h2>


In order to connect to your Snowflake account, you need to enter Snowflake connection information and initialize the connection. 


Follow our :doc:`step-by-step guide</resources/SnowflakeInfo>` on how to find your Snowflake connections information.


.. code-block:: python

	import modin.pandas as pd
	import ponder.snowflake
	from ponder.utils.core import Teleporter

	# Create a Ponder Snowflake Connections object
	snowflake_con = ponder.snowflake.connect(
	    user=*****, #your username that you entered during sign up
	    password=*****, #password that you entered during sign up
	    account=*****, #You can find this under “Admin” > “Accounts” > "Locator" field (You can also find your account in the URL: https://app.snowflake.com/us-west-2/<account-name>/organization, put the <account-name>, not including the URL
	    role=*****, # your access control level. By default this is “ACCOUNTADMIN”.
	    database=*****, # database = “TEST” or whatever you named the database in Step 1
	    schema=*****,   # schema= “PUBLIC”,
	    warehouse=***** # warehouse= “COMPUTE_WH”
	)

	# Initialize the Snowflake connection
	ponder.snowflake.init(snowflake_con, timeout=1200)


Here are more examples on how to :doc:`upload files to your Snowflake account </examples/example1>` or :doc:`reading existing tables on Snowflake </examples/example2>`.

.. _here: https://github.com/modin-project/modin/pulls