Bokeh
=====

`Bokeh <https://docs.bokeh.org/en/latest/>`_ ist eine interaktive
Visualisierungsbibliothek für moderne Webbrowser. Ihr Ziel ist es, vielseitige
Grafiken bereitzustellen und diese Fähigkeit durch performante Interaktivität
auf sehr große und Streaming-Datasets zu erweitern. Bokeh ist hilfreich um
schnell und einfach interaktive Diagramme, Dashboards und Datenanwendungen zu
erstellen.

Um sowohl einfache als auch leistungsstarke und flexible Funktionen zu bieten,
die für erweiterbare Anpassungen erforderlich sind, stellt Bokeh zwei
Interfaces zur Verfügung:

:ref:`bokeh.models <bokeh:bokeh.models>`
    Low-Level-Interface, das Anwendungsentwicklern die größtmögliche
    Flexibilität bietet
:ref:`bokeh.plotting <bokeh:bokeh.models_plots>`
    High-Level-Interface für die Erstellung visueller Glyphen

.. seealso::
   * :doc:`Home <bokeh:index>`
   * :ref:`User Guide <bokeh:userguide>`
   * :doc:`Gallery <bokeh:docs/gallery>`
   * :doc:`Reference Guide <bokeh:docs/reference>`
   * `Source code <https://github.com/bokeh/bokeh>`_
   * Examples

     * `github.com/bokeh/bokeh/tree/main/examples
       <https://github.com/bokeh/bokeh/tree/main/examples>`_
     * `cdn.pydata.org/bokeh/examples/examples-x.y.z.zip
       <https://cdn.pydata.org/bokeh/examples/examples-1.0.4.zip>`_

Installation
------------

Mit :doc:`python4datascience:productive/envs/spack/index` könnt ihr Bokeh in
eurem Kernel bereitstellen, :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

    $ spack env activate python-311
    $ spack install   py-bokeh

Alternativ könnt ihr Bokeh auch mit anderen Paketmanagern installieren,
:abbr:`z.B. (zum Beispiel)`

.. code-block:: console

    $ pipenv install bokeh

Optionale Erweiterungen
~~~~~~~~~~~~~~~~~~~~~~~

Es gibt Erweiterungen für Bokeh für die folgenden Funktionen:

`NodeJS <https://nodejs.org/en/>`_
    Notwendig zum Erweitern von Bokeh oder zum Definieren von
    ``CustomJS``-Implementierungen in CoffeeScript oder TypeScript
`pandas <https://pandas.pydata.org/>`_
    Notwendig für die Hexbin-Funktion. Einige Anwendungen werden durch die
    Verwendung von pandas vereinfacht, :abbr:`z.B. (zum Beispiel)` werden pandas
    DataFrames durch Glyph-Funktionen automatisch in Bokeh-Datenquellen
    konvertiert
`Psutil <https://psutil.readthedocs.io/en/latest/>`_
    Erforderlich, um eine detaillierte Speicherprotokollierung im Bokeh-Server
    zu ermöglichen
`NetworkX <https://networkx.org>`_
    Mit ``from_networkx`` lässt sich der Bokeh-Diagramm-Renderer direkt auf
    NetworkX-Daten anwenden
`Selenium <https://www.selenium.dev/>`_, `PhantomJS <https://phantomjs.org/>`_
    Notwendig für das Exportieren von Plots in PNG- und SVG-Bilder

Beispiele
---------

Bei der Installation mit ``pip`` werden die Beispiele nicht mitinstalliert.
Ihr könnt jedoch das Git-Repository klonen und euch das Verzeichnis
``examples/`` anschauen um die Beispiele zu sehen.

Die meisten dieser Beispiele nutzen Beispieldaten, die ebenfalls separat zur
Verfügung gestellt werden müssen. Um diese Dateien herunterzuladen, gebt
einfach folgendes ein::

    $ pipenv run bokeh sampledata

.. toctree::
    :titlesonly:
    :maxdepth: 0
    :hidden:

    styling-theming.ipynb
    data-sources-transformations.ipynb
    annotations.ipynb
    interactions.ipynb
    graph.ipynb
    geographic-plots.ipynb
    bokeh-server.ipynb
    directory-format-apps.ipynb
    embedding-export/notebook.ipynb
    embedding-export/export-html.ipynb
    embedding-export/static-images.ipynb
    embedding-export/flask
    extend.ipynb
    integration/index
