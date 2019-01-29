==================
Network
==================

* Download all pdf files in the url.

.. code-block:: console

   $wget -A pdf -m -p -E -k -K -np https://jachermocilla.org/publications/

* View network interfaces.

.. code-block:: console

   $ifconfig
   $ip addr

* View routing information.

.. code-block:: console

   $route -n
   $ip route

* View DNS resolver information.

.. code-block:: console

   $cat /etc/resolv.conf

* View the processes listening at a particular port.

.. code-block:: console

   $sudo netstat -tunlp
