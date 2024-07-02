seaborn-Installation
====================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr seaborn in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-seaborn

Alternativ könnt ihr seaborn auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit :doc:`Pipenv
<python4datascience:productive/envs/pipenv/index>`.

.. note::
   Falls ihr pipenv noch nicht installiert habt, findet ihr eine Anleitung
   hierzu unter :doc:`Pipenv-Installation
   <python4datascience:productive/envs/pipenv/index>`.

.. code-block:: console

    $ pipenv install seaborn

Die Installation könnt ihr überprüfen mit

.. code-block:: pycon

    >>> import seaborn as sns
