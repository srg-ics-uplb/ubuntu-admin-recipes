=====================
Filesystem
=====================

* Find all files in `/var` modified since 28 days ago or less that are greater than 50MB and perform an `ls` on each found files.

.. code-block:: console

   $find -type f -mtime -28 -size +50M -exec ls -lh {} \;
