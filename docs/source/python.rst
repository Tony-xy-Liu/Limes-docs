.. _py-title:

Using the Python Client
=======================

.. _py-install:

Install
-------

.. code-block:: console
    
    (env)$ pip install limes-inventory

.. Tip::
    We recommend performing the installation within a virtual environment which can be 
    created by `venv <https://docs.python.org/3/library/venv.html>`_ or
    `conda <https://www.anaconda.com/>`_.


.. _py-import:

Import
------

.. code-block:: python

    from limes import Limes


.. _py-login:

Login
-----

.. code-block:: python
    
    Limes.Login('username', 'password')


.. _py-search:

Search
------

.. code-block:: python
    
    result = Limes.Search('guag')
    result.ToDict()
