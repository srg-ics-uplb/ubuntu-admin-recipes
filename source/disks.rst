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


