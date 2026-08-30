pandas-Installation
===================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr pandas in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-pandas

Alternativ könnt ihr pandas auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit :doc:`uv
<python4datascience:productive/envs/uv/index>`.

.. note::
   Falls ihr uv noch nicht installiert habt, findet ihr eine Anleitung hierzu
   unter :ref:`uv-Installation <python-basics:uv>`.

.. code-block:: console

    $ uv add pandas

Die Installation könnt Ihr dann überprüfen mit:

.. code-block:: pycon

    >>> import pandas as pd
