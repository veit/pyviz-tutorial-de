Graphviz
========

``Graph-`` und ``Digraph``-Objekte haben eine ``_repr_svg_()``-Methode, sodass
sie direkt in einem Jupyter-Notebook gerendert und dargestellt werden können.

Installation
------------

.. tab:: Spack

   Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr Graphviz
   in eurem Kernel bereitstellen:

   .. code:: console

      $ spack env activate python-311
      $ spack env status
      ==> In environment python-311
      $ spack install py-graphviz
      …
      ==> Successfully installed py-graphviz
      …
      ==> Updating view at /srv/jupyter/spack/var/spack/environments/python-311/.spack-env/view

.. tab:: Debian/Ubuntu

   Zunächst wird Graphviz installiert mit:

   .. code:: console

      $ sudo apt install graphviz

   Anschließend könnt ihr dann in eurem Kernel das zugehörige Python-Paket
   installieren:

   .. code:: console

      $ pipenv install graphviz

.. tab:: macOS

   Zunächst wird Graphviz mit `Homebrew <https://brew.sh/>`_ installiert:

   .. code:: console

      $ brew install graphviz

   Anschließend könnt ihr dann in eurem Kernel das zugehörige Python-Paket
   installieren:

   .. code:: console

      $ pipenv install graphviz

.. toctree::
    :titlesonly:
    :maxdepth: 0
    :hidden:

    examples.ipynb
    libs-tools
