===============
Users
===============

* Add a new user (ex. mbbdr) with sudo access.

.. code-block:: console

   $sudo adduser mbbdr
   $sudo usermod -aG sudo mbbdr

* View the user id of a user (ex. mdq).

.. code-block:: console

   $id mdq


* Where are the password hashes stored?

.. code-block:: console

   $cat /etc/passed;cat /etc/groups;sudo cat /etc/shadow
