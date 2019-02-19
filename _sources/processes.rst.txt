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

* List the status of available services.

.. code-block:: console

   $sudo service --status-all

* Show process tree rooted at a given process id 30872.

.. code-block:: console

   $ps f --forest -g $(ps -osid= -p 30872)
   $pstree 30872

* Generate a core dump of a running process with PID=1234

.. code-block:: console

   $sudo gcore 1234 
