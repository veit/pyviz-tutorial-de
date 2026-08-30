GeoPandas-Installation
======================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr GeoPandas in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-geopandas

Alternativ könnt ihr GeoPandas auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit
:doc:`python4datascience:productive/envs/uv/index`:

.. code-block:: console

    $ uv add fiona matplotlib descartes geopandas

.. note::
   Falls ihr uv noch nicht installiert habt, findet ihr eine Anleitung hierzu
   unter :ref:`uv-Installation <python-basics:uv>`.

Die Installation könnt ihr dann überprüfen mit:

.. code-block:: pycon

    >>> import geopandas as gpd
