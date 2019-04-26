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

* To Disable IPv6 add the following lines to `/etc/sysctl.conf`.

.. code-block:: console

   net.ipv6.conf.all.disable_ipv6 = 1
   net.ipv6.conf.default.disable_ipv6 = 1
   net.ipv6.conf.lo.disable_ipv6 = 1

Run the following:

.. code-block:: console

   $sudo sysctl -p

* Mirror a site

.. code-block:: console

   wget --mirror --convert-links --adjust-extension --page-requisite --no-parent http://example.org
