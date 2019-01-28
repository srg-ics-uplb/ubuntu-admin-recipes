=================
Memory
=================

* View memory available and used.

.. code-block:: console

   $free -m

* View memory memory used by a process (ex. firefox).

.. code-block:: console

   $pmap `ps -A | grep firefox | awk '{print $1}'`

