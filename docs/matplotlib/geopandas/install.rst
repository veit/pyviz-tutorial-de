GeoPandas-Installation
======================

Mit :doc:`jupyter-tutorial:productive/envs/spack/index` könnt ihr GeoPandas in
eurem Kernel bereitstellen, z.B. mit:

.. code-block:: console

    $ spack env activate python-38
    $ spack install py-geopandas@0.9.0%gcc@11.2.0

Alternativ könnt ihr GeoPandas auch mit anderen Paketmanagern installieren, z.B.
mit :doc:`jupyter-tutorial:productive/envs/pipenv/index`:

.. code-block:: console

    $ pipenv install fiona matplotlib descartes geopandas

.. note::
    Falls ihr pipenv noch nicht installiert habt, findet ihr eine Anleitung
    hierzu unter :ref:`pipenv-installieren`.

Die Installation könnt ihr dann überprüfen mit:

.. code-block:: python

    >>> import geopandas as gpd

