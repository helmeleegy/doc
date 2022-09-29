.. Ponder Docs documentation master file, created by
   sphinx-quickstart on Wed Sep  7 15:45:48 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.



Introduction to Ponder!
=======================
.. toctree::
   :hidden:
   :maxdepth: 100

   deployment/cloud
   examples/example1
   overviewAPI/dataframes
   security/security
   help/support



Ponder is a highly scalable Dataframe-as-a-Service that builds on top of Modin, the popular open source technology for running distributed pandas.

With Ponder, data teams no longer have to pull their data out of the warehouse to work with it in pandas. **Ponder’s breakthrough Database Pushdown capability allows users to run pandas** directly *in* the warehouse, meaning that we inherit all the scalability and security benefits of the database, while still preserving the `ease-of-use <https://ponder.io/pandas-vs-sql-part-4-pandas-is-more-convenient/>`_ and `flexibility <https://ponder.io/pandas-vs-sql-part-3-pandas-is-more-flexible/>`_ of pandas. 


With Ponder, your data teams will be able to unleash the power of pandas with:

- **Scale:** Effortlessly transition workflows from prototype to production
- **Speed:** Improve productivity + accelerate developer velocity
- **Security:** Run securely on any infrastructure or inside of your warehouse
- **Reliability:** Monitor dataframe health like any other mission critical system



.. figure:: img/ponderGif.gif
   :width: 400px
   :align: center


Offered Services
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

Your team can leverage Ponder’s technology in two ways: 

**Ponder on Cloud:** Ponder hosts your dataframes end to end. User interacts directly with our managed Ponder Studio to get access to DB pushdown capabilities.

.. image:: img/ponderCloud.png
   :width: 800px
   :alt: ponder cloud
   :align: center

**Ponder Enterprise:**  Ponder deploys in your VPC and gives you the flexibility of executing your pandas code using Compute Engine, Dataproc, Big Query, and more.

.. image:: img/ponderEnterprise.png
   :width: 800px
   :alt: ponder enterprise
   :align: center