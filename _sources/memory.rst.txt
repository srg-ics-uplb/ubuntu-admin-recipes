=================
Memory
=================

* View memory available and used.

.. code-block:: console

   $free -m

* View memory memory used by a process (ex. firefox).

.. code-block:: console

   $pmap `ps -A | grep firefox | awk '{print $1}'`

* View the memory used by each user. 
  (Source: https://stackoverflow.com/questions/14214315/how-to-find-user-memory-usage-in-linux/14214516)

.. code-block:: console

   $echo "USER                 RSS      PROCS" ; echo "-------------------- -------- -----" ; ps hax -o rss,user | awk '{rss[$2]+=$1;procs[$2]+=1;}END{for(user in rss) printf "%-20s %8.0f %5.0f\n", user, rss[user]/1024, procs[user];}' | sort -rnk2

 
