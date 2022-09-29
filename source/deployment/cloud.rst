##########################
 Getting Started
##########################

.. toctree::
    :hidden:
    :maxdepth: 100
   
   
   	Ponder Cloud - Managed Notebook <self>
    enterprise


.. raw:: html

	In this guide you will:
	<ol>
		<li>Sign up for Ponder Account</li>
		<li>Create Snowflake Account (if you haven’t already)</li>
		<li>Launch Ponder Studio</li>
		<li>Open a Jupyter notebook</li>
		<li>Connect to your DB and start Pondering 🎉</li>
	</ol>

.. raw:: html

	<h2>Step 1: Sign up for Ponder Account</h2>


If you haven’t already, please go to `Ponder's product page <https://ponder.io/>`_ and sign up for Ponder using your email address.

.. raw:: html

	<h2>Step 2: Create Snowflake Account (if you haven’t already)</h2>


If you have a snowflake account you can skip this step. Otherwise, you first need to create a snowflake account. Follow our :doc:`step-by-step guide</resources/SnowflakeAccountCreation>` on how to create an account on Snowflake. 

.. raw:: html

	<h2>Step 3: Launch Ponder Studio</h2>


After signing in to your account, go to the "Workspace" tab and press "Launch Ponder Studio" button. This will open a new tab that shows your Jupyter directory. 



.. raw:: html

	<h2>Step 4: Open a Jupyter notebook</h2>
You can either open an existing template notebook called ``example_db_pushdown.ipynb`` that exists on your Jupyter directory or open a new notebook. ``example_db_pushdown.ipynb`` notebook already contains an template code snippest for connecting to your Snowflake database. 


You need to set the notebook kernel to ``pdkernel``. This is under ``Kernel`` > ``Change kernel`` tab at the top of your notebook page. See figure below for more details.

.. image:: /img/UI/uiScreen.png
	:width: 800px
	:alt: snowflake
	:align: center




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




