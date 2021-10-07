.. _con-title:

On the Network
==============

.. _con-elab:

ELab
----

A wrapper inheriting ``Connections`` was created to provide typing for
`eLab's API <https://www.elabjournal.com/docs/api/index>`_ and integrate it as a
``Provider``.

`Click here to go to eLab <https://elab.msl.ubc.ca/>`_

.. _con-server:

Server
------

The server runs on a VM where access is only possible via SSH. It impliments the
``Provider`` interface (specified by the ``Connections`` module) with additional
endpoints for the :ref:`portal<port-title>` and printers. This is meant to be the
persistent source of truth for the network, though communications with other network
elements need not always go through the server.

The server utilizes both ``REST`` and ``SocketIO`` protocols.

`Click here to go to the Limes Portal <http://sh-lims.microbiology.ubc.ca:8001/>`_

:ref:`What's a "Limes Portal" and how do I use it?<port-title>`

.. _con-shamwow:

Shamwow
-------

An ``SshConnection`` module allows for Shamwow to be connected as a ``Provider`` by
emulating a bash console and connecting via ssh. While not explicitly implimented, the
``SshConnection`` module allows Limes to access Shamwow on behaf of a user
(using their ssh credentials) and run commands.

.. _con-printers:

Printers
--------

A `python driver <https://github.com/Tony-xy-Liu/Limes-Printer>`_ handles print requests
from the server via ``SocketIO``. For each request, it generates a barcode, QR code, and
label from an existing template using
`Apache OpenOffice Writer <https://www.openoffice.org/>`_ before sending a print command
over USB.

:ref:`How to print labels<port-labels>`
