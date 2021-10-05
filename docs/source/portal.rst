.. _port-title:

Limes Portal
=============

link: `<http://sh-lims.microbiology.ubc.ca:8001/>`_

Log in using your eLab credentials.

.. Note::
    - A connection to the UBC Secure network is required, via VPN, campus wifi, or ethernet cable.


Search by Storage Location
--------------------------

Search for samples in a storage location by entering the address of the location.
The address need not be precise. For example,

.. code-block:: none

    11, 2, 3

would suffice for

.. code-block:: none

    -80C Freezer #11, shelf 2, rack 3

Results are displayed in a table at the bottom

.. Note::
    If a storage is not found, pressing the :code:`Reload Storages`
    button will have Limes synchronize its remembered storage locations with eLab.

Pressing :code:`Print` will display the barcodes of all samples found in the print page

Print Labels
------------

Enter each sample to print by pasting it's barcode on a new line like so:

.. code-block:: none

    005000009764829
    005000009764830
    005000009764831

Add additional text by appending it after a comma:

.. code-block:: none

    005000009764829
    005000009764830, custom text
    005000009764831, more custom text

.. Note::
    
    If a barcode is matched to a sample on eLab, the sample's name will be automatically
    sent to the label, otherwise, only the custom text will be sent.

The information to be printed for each label will be shown in the table at the bottom.

Pressing :code:`Copy to Clipboard` button will allow you to paste the label information
into a spreadsheet for editing. It should be possible to then directly paste the updated
contents back into the *Samples* box.

A :code:`Label Template` and :code:`Printer` must be selected before printing.

.. Note::

    Ensure that the selected template matches the physical labels loaded in the printer.

When ready, press :code:`Print All` and wait for confirmation.