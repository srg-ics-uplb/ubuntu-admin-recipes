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
