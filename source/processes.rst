======================
Processes and Services
======================

* View on what processors a process (ex. firefox) is running.

.. code-block:: console

   $watch "ps -ax -o pid,psr,comm | grep firefox"


* View the processes running on `CORENUM`.

.. code-block:: console

   $CORENUM=1;ps -e -o pid,psr,comm,cmd | grep -E  "^[[:space:]][[:digit:]]+[[:space:]]+${CORENUM}"

* Run a process (ex. google-chrome) on a specific core only.

.. code-block:: console
   
   $taskset --cpu-list 2 /usr/bin/google-chrome

* Start and stop the apache (or any service).

.. code-block:: console

   $sudo service apache start
   $sudo service apache stop

