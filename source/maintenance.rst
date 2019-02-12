==========================
Maintenance and Accounting
==========================

* View `syslog` contents continuously.

.. code-block:: console

   $sudo tail -f /var/log/syslog

* View kernel ring buffer which contains information during bootup such as what devices were detected.

.. code-block:: console

   $dmesg

* Update the packages.

.. code-block:: console

   $sudo apt-get update && sudo apt-get upgrade -y

* View system calls used by a process.

.. code-block:: console

   $strace cp hello.txt hello2.txt

* View system status and performance.

.. code-block:: console

   $top

