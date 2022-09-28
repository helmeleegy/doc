Snowflake connection information
===============

Details on how to find your Snowflake connections information 

``user`` is your username that you entered during sign up (You can find this under “Profile”).


``password`` is the password that you entered during sign up. 


``account`` is your `account identifier <https://docs.snowflake.com/en/user-guide/admin-account-identifier.html>`_. To find your account, you need to:

   **Step 1:** Go to  ``Admin`` > ``Accounts``

   .. image:: /img/Snowflake/info/screen1.png
      :width: 800px
      :alt: snowflake
      :align: center

   
   **Step 2:** Copy the ``LOCATOR`` address

   .. image:: /img/Snowflake/info/screen2.png
      :width: 800px
      :alt: snowflake
      :align: center

   **Step 3:** Select the ``account`` identifier from the copied LOCATOR address

   .. code-block:: bash
   
      Copied LOCATOR address: https://rq08674.us-east-2.aws.snowflakecomputing.com

      #This is what we need for Snowflake connection
      account = "rq08674.us-east-2.aws" 





``role`` is your access control level. 
 
.. code-block:: bash

   #By default 
   role = "ACCOUNTADMIN"

For the database, we are just using the sample data provided by Snowflake for the purpose of establishing the connection. Go to ``Data`` > ``Databases``:

.. code-block:: bash

   #By default 
   database="TEST",
   schema= "PUBLIC"


To get warehouse information, go to ``Admin`` > ``Warehouses`` and find the name of the Warehouse. 

.. code-block:: bash

   #By default 
   warehouse="COMPUTE_WH"
  

Finally, the connection string should look something like this: 

.. code-block:: bash

   snowflake_con = ponder.snowflake.connect(
    user="BAHADORSAKET",
    password="**********",
    account="rq08674.us-east-2.aws",
    role="ACCOUNTADMIN",
    database="TEST",
    schema= "PUBLIC",
    warehouse= "COMPUTE_WH"
   )


