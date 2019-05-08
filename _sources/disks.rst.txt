===============
Disks
===============


* Show disk partitions

.. code-block:: console
   
   $sudo fdisk -l

* View available disk space.


.. code-block:: console
   
   $df -h

* Write an image or .iso to disk.

.. code-block:: console

   $sudo dd if=disk.img of=/dev/sdb1

* Get the number of blocks used by a file

.. code-block:: console

   $sudo debugfs -R "stat hello.txt" /dev/sda

* Get the block size

.. code-block:: console

   $sudo blockdev --getbsz /dev/sda


* Get statistics for I/O

.. code-block:: console

   $sudo apt install sysstat && sudo iostat -u


* View available I/O schedulers

.. code-block:: console

   $cat /sys/block/sda/queue/scheduler

* Get statistics of disk

.. code-block:: console

   $sudo hdparm -tT /dev/sda

