plotnine-Installation
=====================

In den meisten Fällen sollte folgende Installation hinreichend sein:

.. code:: console

    $ uv add plotnine

Für die Verwendung zusammen mit `scikit-learn <https://scikit-learn.org/>`_ und
`scikit-misc <https://github.com/has2k1/scikit-misc>`_ können Extras installiert
werden mit

.. code:: console

    $ uv add "plotnine[all]"

.. tab:: Jupyter-Notebooks

   .. code:: console

      $ jupyter nbextension enable --py widgetsnbextension

.. tab:: JupyterLab

   .. code:: console

      $ jupyter labextension install @jupyter-widgets/jupyterlab-manager
