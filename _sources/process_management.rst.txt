
==================
Process Management
==================

* View on what processor the firefox process is running.

.. code-block:: console

   $watch "ps -ax -o pid,psr,comm | grep firefox"


* View the processes running on `CORENUM`.

.. code-block:: console

   $CORENUM=1;ps -e -o pid,psr,comm,cmd | grep -E  "^[[:space:]][[:digit:]]+[[:space:]]+${CORENUM}"
