Matplotlib-Installation
=======================

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr Matplotlib
in eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install py-matplotlib

Alternativ könnt ihr Matplotlib auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)` mit :doc:`Pipenv
<python4datascience:productive/envs/pipenv/index>`:

.. code-block:: console

    $ pipenv install matplotlib

Die Installation könnt ihr dann überprüfen mit:

.. code-block:: python

    >>> import matplotlib.pyplot as plt

.. note::
    Wenn ihr den Fehler ``TclError: no display name and no $DISPLAY
    environment variable`` erhaltet, müsst ihr vermutlich das iPython-Backend
    für Matplotlib verwenden mit

    .. code-block:: python

       import matplotlib.pyplot as plt

       # iPython backend for matplotlib
       %matplotlib inline

    Sofern Ihr Matplotlib in einer Python-Datei importiert, müsst ihr
    stattdessen folgendes einfügen:

    .. code-block:: python

       import matplotlib.pyplot as plt


       # iPython backend for matplotlib
       get_ipython().run_line_magic("matplotlib", "inline")
