Cartopy-Installation
====================

.. tab:: Spack

   Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr Cartopy
   in eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

   .. code-block:: console

       $ spack env activate python-311
       $ spack install py-cartopy~epsg~ows~plotting

   Dies installiert Cartopy mit Unterstützung von:

   * `epsg <https://epsg.io>`_
   * `Open Geospatial Consortium (OGC) <https://www.ogc.org>`_
   * Plot-Funktionalität

   Zusätzlich werden folgende Pakete mitinstalliert:

   * `gdal <https://gdal.org/en/latest/>`_
   * :doc:`/matplotlib/index`
   * `OWSLib <https://geopython.github.io/OWSLib/>`_
   * `Pillow <https://pillow.readthedocs.io/en/stable/>`_
   * `pyepsg <https://pyepsg.readthedocs.io/en/latest/>`_
   * `PyShp <https://github.com/GeospatialPython/pyshp>`_
   * `shapely <https://shapely.readthedocs.io/en/stable/>`_
   * `six <https://six.readthedocs.io>`_

.. tab:: Linux

   Cartopy kann alternativ auch mit Linux-Paketmanagern installiert werden,
   :abbr:`z.B. (zum Beispiel)` für  Debian≥9 (Stretch) mit:

   .. code-block:: console

       $ sudo apt install proj-bin
       $ sudo apt install libproj-dev
       $ sudo apt install libgeos-dev

.. tab:: macOS

   .. code-block:: console

       $ brew install proj
       $ brew install geos

Anschließend kann Cartopy für euren Kernel installiert werden, :abbr:`z.B. (zum
Beispiel)` mit:

.. code-block:: console

    $ export PIP_NO_BINARY=:shapely:
    $ pipenv install cython numpy cartopy

Für die :doc:`examples` benötigt ihr dann zusätzlich die folgenden beiden
Python-Pakete:

.. code-block:: console

    $ pipenv install matplotlib scipy

Optionale Anforderungen
-----------------------

* `rtree <https://github.com/Toblerity/rtree>`_ für `libspatialindex
  <https://github.com/libspatialindex/libspatialindex>`_
* `psycopg2 <https://pypi.org/project/psycopg2/>`_ für `PostGIS
  <https://postgis.net/>`_
* `geopy <https://github.com/geopy/geopy>`_

Anforderungen zum Plotten
-------------------------

* :doc:`/matplotlib/index`
* `descartes <https://pypi.org/project/descartes/>`_
* `mapclassify <https://pysal.org/mapclassify/>`_

Überprüfen
----------

Schließlich könnt ihr die Installation überprüfen mit:

.. code-block:: pycon

    >>> import cartopy
