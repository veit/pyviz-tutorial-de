pandas-Installation
===================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr pandas in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-pandas

Alternativ könnt ihr pandas auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit :doc:`Pipenv
<python4datascience:productive/envs/pipenv/index>`.

.. note::
   Falls ihr pipenv noch nicht installiert habt, findet ihr eine Anleitung
   hierzu unter :doc:`Pipenv-Installation
   <python4datascience:productive/envs/pipenv/install>`.

.. code-block:: console

    $ pipenv install pandas

Die Installation könnt Ihr dann überprüfen mit:

.. code-block:: pycon

    >>> import pandas as pd
