=====================
Filesystem
=====================

* Find all files in `/var` modified since 28 days ago or less that are greater than 50MB and perform an `ls` on each found file.

.. code-block:: console

   $find /var -type f -mtime -28 -size +50M -exec ls -lh {} \;

* View sizes of directories.

.. code-block:: console

   $du -h

* Find mounted partitions.

.. code-block:: console

   $findmnt
   $cat /etc/mtab

* View disks and partitions.

.. code-block:: console

   $sudo fdisk -l

* Create a DOS disk image.

.. code-block:: console

   $mkfs.msdos -C myfloppy.img 1440

* Mount/Unmount a disk image through a loop device.

.. code-block:: console

   $mkdir mnt_tmp
   $sudo mount -oloop myfloppy.img mnt_tmp/
   $sudo umount mnt_tmp/
