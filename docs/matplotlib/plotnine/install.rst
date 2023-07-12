plotnine-Installation
=====================

In den meisten Fällen sollte folgende Installation hinreichend sein:

.. code:: console

    $ pipenv install plotnine

Für die Verwendung usammen mit `scikit-learn <https://scikit-learn.org/>`_ und
`scikit-misc <https://github.com/has2k1/scikit-misc>`_ können Extras installiert
werden mit

.. code:: console

    $ pipenv install "plotnine[all]"

.. tab:: Jupyter-Notebooks

   .. code:: console

      $ jupyter nbextension enable --py widgetsnbextension

.. tab:: JupyterLab

   .. code:: console

      $ jupyter labextension install @jupyter-widgets/jupyterlab-manager
