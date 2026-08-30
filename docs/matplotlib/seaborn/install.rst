seaborn-Installation
====================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr seaborn in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-seaborn

Alternativ könnt ihr seaborn auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit :doc:`uv
<python4datascience:productive/envs/uv/index>`.

.. note::
   Falls ihr uv noch nicht installiert habt, findet ihr eine hierzu unter
   :ref:`uv-Installation <python-basics:uv>`.

.. code-block:: console

    $ uv add seaborn

Die Installation könnt ihr überprüfen mit

.. code-block:: pycon

    >>> import seaborn as sns
