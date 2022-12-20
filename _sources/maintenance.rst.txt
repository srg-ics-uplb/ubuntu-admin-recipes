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
   $htop

* View the list of packages installed via apt
  (See https://askubuntu.com/questions/17012/is-it-possible-to-get-a-list-of-most-recently-installed-packages)

.. code-block:: console

   $zcat -f /var/log/dpkg.log* | grep " install " | sort > /tmp/dpkg.log
   $grep -F "`comm -12 <(apt-mark showmanual | sort) <(cat /tmp/dpkg.log | cut -d " " -sf4 | grep -o "^[^:]*" | sort)`" /tmp/dpkg.log | grep \<none\>

* Find large packages.

.. code-block:: console

   $dpkg --list |grep "^rc" | cut -d " " -f 3 | xargs sudo dpkg --purge
   $dpkg-query -Wf '${Installed-Size}\t${Package}\n' | sort -nr | less


