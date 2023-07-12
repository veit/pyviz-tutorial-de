seaborn-Installation
====================

Mit :doc:`jupyter-tutorial:productive/envs/spack/index` könnt ihr seaborn in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-38
    $ spack install py-seaborn@0.11.2%gcc@11.2.0

Alternativ könnt ihr seaborn auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)

.. code-block:: console

    $ pipenv install seaborn

.. note::
    Falls ihr pipenv noch nicht installiert habt, findet ihr eine Anleitung
    hierzu unter :ref:`pipenv-installieren`.

Die Installation könnt ihr überprüfen mit

.. code-block:: python

    >>> import seaborn as sns
