.. _port-title:

Limes Portal
=============

link: `<https://limes-inventory.github.io/>`_

Log in using your eLab credentials.

.. Note::
    - A connection to the UBC Secure network is required, via VPN, campus wifi, or ethernet cable.

.. _port-searchLoc:

Search by Storage Location
--------------------------

:ref:`Log in to the portal<port-title>` and click ``Search By Storage Location``.

Search for a storage location by entering the names of the storage levels to that location, seperated by commas.
This need not be too precise. For example,

.. code-block:: none

    11, 2, 3

would yield

.. code-block:: none

    -80C Freezer #11, shelf 2, rack 3

.. warning::

    Be aware of ambiguities. ``1``, for instance, will match terms like ``Freezer #01`` or
    ``Freezer #15``, and ``8`` will match ``-80C Freezer``! *The search is simply matching the
    name of each storage level.*

The **barcode** and full address of the specified location will appear and all samples
in that specific location will be displayed in a table.

.. Note::

    If a storage is not found, pressing the :code:`Reload Storages`
    button will have Limes synchronize its remembered storage locations with eLab.

Pressing :code:`Print` will display the barcodes of all samples found.

.. _port-scan:

Scanning Labels
---------------

:ref:`Log in to the portal<port-title>` and click ``Scanner``.

Barcodes can be entered directly into the box: ``Enter Barcode Here``. After the specified delay
indicated by the box ``Delay (ms)``, the barcode will be entered into the table. This barcode will
be automatically checked against elab and a checkmark (✔) will appear in the ``Added?`` column if the
barcode was found in eLab.

When ready to confirm the reception of barcodes (and their samples by proxy), select the desired barcodes
from the scanned barcodes table and click ``Confirm Recieve``. **The MMAP API will then be notifed of these barcodes.**
The ``Info`` column will display identifiers for the barcode if the MMAP API was succesfully updated, or
continue to display ``unknown`` on failure.

.. warning::

    The MMAP API will only accept confirmation once, so there is no way to tell the difference between
    a succesful confirmation and a repeat confirmation. Attempts to improve this was met with logistical
    resistence.
    
Selected barcodes with retrieved metadata (ex. names or other identifiers) can be copied to the clipboard as a table
to be later pasted into a spreadsheet for bulk entry into eLab.

.. Note::

    Double clicking on any row will open the eLab page for that barcode if found in eLab.

.. Note::

    Use the ``Toggle Camera`` button to scan barcodes directly using the built-in camera of the device.

.. Note::

    The scanned list of barcodes will persist between login sessions and devices for each user, *as long as the
    server has not restarted.*

.. _port-labels:

Printing Labels
---------------

Ensure that a template for the style of label you wish to print has been created.

`How do I make a template? <https://elab.msl.ubc.ca/members/protocol/?protID=40950>`_

:ref:`Log in to the portal<port-title>` and click ``Print``.

In the ``Items`` field, enter each item to print by pasting its' **barcode** on a new line like so:

.. code-block:: none

    005000009764829
    005000009764830
    005000009764831

.. Tip::

    Consider using the :ref:`Search By Storage Locaton<port-searchLoc>` feature to acquire
    barcodes of many samples of storage locations like boxes / racks.
    :ref:`Have a look at this example for a walkthrough<ex-env>`

.. Note::
    
    If a barcode is matched to a sample on eLab, the sample's name will be automatically
    sent to the label, otherwise, only the custom text will be sent.

Add additional text by separating it with a comma or the ``tab`` character. *Pasting entries
directly from a spreadsheet is possible here.*

.. code-block:: none

    005000009764829
    005000009764830, custom text
    005000009764831, text for "o.text2", text for "o.text3"
    005000009764831 tab separated & from a spreadsheet

.. Note::

    It is possible to print *unlinked* labels, though this is **highly NOT recommended.** 
    Simply enter your own barcode or start with a comma to indicate a blank barcode, for example:

    .. code-block:: none

        12345, a lonely label not connected to eLab
        , a sad label with no barcode

The information to be printed for each label will be shown in the table at the bottom.

Pressing the :code:`Copy to Clipboard` button will allow you to paste the label information
into a spreadsheet for editing. It should then be possible to directly paste the updated
contents back into the ``Items`` box.

A :code:`Label Template` and :code:`Printer` must be selected before printing.

.. Note::

    Ensure that the selected template matches the physical labels loaded in the printer.

When ready, press :code:`Print All` and wait for confirmation.

.. _port-change-labels:

Changing Labels
---------------

`View the protocol on eLab <https://elab.msl.ubc.ca/members/protocol/?protID=40983>`_

.. _port-troubleshoot:

Troubleshooting
---------------

`View Troubleshooting on eLab <https://elab.msl.ubc.ca/members/protocol/?protID=41057>`_

