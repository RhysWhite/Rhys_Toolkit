Creating soft symbolic links
=============================

Soft links are created with the `ln` command. To link a file to your current working directory, use:

.. code-block::

  $ ln -s <Path>/<file> <link>

Then to verify the new soft link, use:

.. code-block::
 
  $ ls -l <Path>/<file> <link>
