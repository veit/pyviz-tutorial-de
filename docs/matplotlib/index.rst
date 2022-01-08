Matplotlib
==========

`Matplotlib <https://matplotlib.org/>`_ ist eine 2D-Plot-Bibliothek, die in
Python-Skripten, iPython-Shells und Jupyter-Notebooks verwendet werden kann.
Mit ihr lassen sich Daten als Diagramme, Histogramme, Leistungsspektren,
Balkendiagramme, Streudiagramme etc. visualisieren. Einen Überblick erhaltet ihr
in `Gallery <https://matplotlib.org/stable/gallery/index.html>`_. Es ist eine
Low-Level-Bibliothek mit einem Matlab ähnlichen Schnittstelle, die zwar
einerseits viele Freiheiten bietet, andererseits jedoch viel Code erfordert.

+---------------------------------------+---------------------------------------+
| Pros                                  | Cons                                  |
+=======================================+=======================================+
| Ähnliches Design wie Matlab; der      | Imperative API und häufig sind sehr   |
| Wechsel ist einfach                   | ausführliche Angaben nötig            |
+---------------------------------------+---------------------------------------+
| Viele Rendering-Backends, siehe       | Häufig ungenügende Standarddarstellung|
| :doc:`mpl-backends`                   |                                       |
+---------------------------------------+---------------------------------------+

.. seealso::
   - `Pyplot function overview <https://matplotlib.org/api/pyplot_summary.html>`_
   - `User’s Guide <https://matplotlib.org/users/index.html>`_
   - `Toolkits <https://matplotlib.org/api/toolkits/index.html>`_
   - `Third party packages <https://matplotlib.org/thirdpartypackages/index.html>`_
   - `Nicolas P. Rougier: Scientific Visualization – Python & Matplotlib
     <https://github.com/rougier/scientific-visualization-book>`_
   - `Nicolas P. Rougier: Matplotlib cheat sheet
     <https://github.com/rougier/matplotlib-cheatsheet>`_
   - `Learning matplotlib <https://riptutorial.com/ebook/matplotlib>`_
   - `SciTools courses: An introduction to matplotlib
     <https://github.com/SciTools/courses/blob/master/course_content/extra_courses/matplotlib_intro.ipynb>`_

.. toctree::
    :titlesonly:
    :maxdepth: 0
    :hidden:

    mpl-install
    mpl-backends.ipynb
    mpl-example.ipynb
    mpl-scatter-density
    mpld3 <https://mpld3.github.io/>
    pandas/index
    geopandas/index
    seaborn/index
    ggpy <http://yhat.github.io/ggpy/>
    plotnine/index
    networkx.ipynb
    graphviz.ipynb
    graph-tool.ipynb
    cartopy/index
    iris
    yt
