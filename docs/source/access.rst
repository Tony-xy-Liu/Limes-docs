.. _acc-title:

Using Limes
===============

Access to Limes is possbile either through a web portal or python module.

.. _access-portal:

Web Portal
----------
link: `<http://sh-lims.microbiology.ubc.ca:8001/>`_

.. Note::
    - A connection to the UBC network is required.
    - Login using ELab credentials

.. _access-python:

Python
------

Install:

.. code-block:: console
    
    (env)$ pip install limes-inventory

.. Note::
    We recommend performing the installation within a virtual environment such as
    that provided by `venv <https://docs.python.org/3/library/venv.html>`_ or
    `conda <https://www.anaconda.com/>`_.

Login using your eLab credentials and do a simple search:

.. code-block:: python

    from limes import Limes
    Limes.Logn('username', 'password')
    Limes.search('guag')

.. _access-elab:

ELab
----

- link: `<https://elab.msl.ubc.ca/>`_

- documentation: `<https://www.elabjournal.com/doc/>`_

.. Creating recipes
.. ----------------

.. To retrieve a list of random ingredients,
.. you can use the ``lumache.get_random_ingredients()`` function:


.. The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
.. or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
.. will raise an exception.

.. For example:

.. >>> import lumache
.. >>> lumache.get_random_ingredients()
.. ['shells', 'gorgonzola', 'parsley']

