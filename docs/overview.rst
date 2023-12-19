Überblick über die Bibliotheken zur Datenvisualisierung
=======================================================

Zunächst erhaltet ihr einen grafischen Überblick auf Basis der zentralen
Python-Bibliotheken zur Datenvisualisierung.

.. seealso::
   * `Jake VanderPlas: Python’s Visualization Landscape (PyCon 2017)
     <https://speakerdeck.com/jakevdp/pythons-visualization-landscape-pycon-2017>`_
   * `The Data Visualisation Catalogue
     <https://datavizcatalogue.com/>`_

.. _technologies:

Technologien
------------

.. graphviz::
   :layout: neato

    graph python_visualisation_landscape {

    graph [fontname = "Calibri", fontsize="16", overlap=false];
        node [fontname = "Calibri", fontsize="16", style="bold", penwidth="5px"];
        edge [fontname = "Calibri", fontsize="16", style="bold", penwidth="5px"];
        tooltip="Python Visualisation Landscape";

        // OpenGL
        opengl [
            label="OpenGL",
            tooltip="Open Graphics Library",
            color="#FF66B3",
            target="_top",
            href="../opengl/index.html"]
        VisPy [
            label="Vispy",
            tooltip="Python-Bibliothek für\ninteraktive wissenschaftliche\nVisualisierungen",
            color="#FF66B3",
            target="_top",
            href="http://vispy.org/"]
        mayavi [
            label="Mayavi",
            tooltip="Python-Bibliothek für die\n3D-Visualisierung\nwissenschaftlicher Daten",
            color="#FF66B3",
            target="_top",
            href="http://docs.enthought.com/mayavi/mayavi/"]
        itkwidgets [
            label="itkwidgets",
            tooltip="Interaktive Jupyter-Widgets\nzur Visualisierung von Bildern,\nPunktmengen und Netzen\nin 2D und 3D",
            color="#FF66B3",
            target="_top",
            href="https://itkwidgets.readthedocs.io/en/latest/"]
        vedo [
            label="vedo",
            tooltip="Python-Modul für die\nwissenschaftliche\nAnalyse von 3D-Daten",
            color="#FF66B3",
            target="_top",
            href="https://vedo.embl.es"]
        polyscope [
            label="Polyscope",
            tooltip="Ein C++ und Python-Viewer\nfür 3D-Daten wie Netze\nund Punktwolken",
            color="#FF66B3",
            target="_top",
            href="https://polyscope.run"]
        glumpy [
            label="Glumpy",
            tooltip="Schnittstelle zwischen\nnumpy und OpenGL",
            color="#FF66B3",
            target="_top",
            href="https://glumpy.github.io/"]
        opengl -- VisPy [color="#FF66B3"]
        opengl -- mayavi [color="#FF66B3"]
        opengl -- itkwidgets [color="#FF66B3"]
        opengl -- vedo [color="#FF66B3"]
        opengl -- polyscope[color="#FF66B3"]
        opengl -- glumpy [color="#FF66B3"]

        // Matplotlib
        mpl [
            label="Matplotlib",
            tooltip="Python-Bibliothek\nfür 2D-Plots",
            color="#BF80FF"
            target="_top",
            href="../matplotlib/index.html"]
        mpl_scatter_density [
            label="mpl-scatter-density",
            tooltip="Streudichtekarten für die\naussagekräftige Darstellungen\ngroßer Datensätze",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/mpl-scatter-density.html"]
        pandas [
            label="pandas",
            tooltip="pandas Datenstrukturen mit\nMatplotlib visualisieren",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/pandas/index.html"]
        geopandas [
            label="GeoPandas",
            tooltip="GeoPandas erweitert pandas um geometrische Datentypen",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/geopandas/index.html"]
        geoplot [
            label="Geoplot",
            tooltip="High-level-Bibliothek zum Plotten von Geodaten",
            color="#BF80FF",
            target="_top",
            href="https://residentmario.github.io/geoplot/index.html"]
        prettymaps [
            label="prettymaps",
            tooltip="Python-Bibliothek zum Zeichnen benutzerdefinierter Karten aus OpenStreetMap-Daten",
            color="#BF80FF",
            target="_top",
            href="https://github.com/marceloprates/prettymaps"]
        seaborn [
            label="seaborn",
            tooltip="High-level-Datenvisualisierung\nbasierend auf Matplotlib",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/seaborn/index.html"]
        plotnine [
            label="plotnine",
            tooltip="Python-Implementierung von ggplot2",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/plotnine/index.html"]
        yellowbrick [
            label="Yellowbrick",
            tooltip="Tools für die visuelle Analyse und Diagnose\nvon Scikit-learn-Projekten",
            color="#BF80FF",
            target="_top",
            href="https://www.scikit-yb.org/"]
        networkx [
            label="NetworkX",
            tooltip="Erstellen, Ändern und Analysieren\nkomplexer Netzwerke",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/networkx.html"]
        graphviz [
            label="Graphviz",
            tooltip="Mächtige Visualisierungssoftware\nfür Graphen",
            color="#cccccc",
            target="_top",
            href="../matplotlib/graphviz.html"]
        graph_tool [
            label="graph-tool",
            tooltip="Effizientes Python-Modul zur\nManipulation und statistischen Analyse\n von Graphen",
            color="#cccccc",
            target="_top",
            href="../matplotlib/graph-tool.html"]
        cartopy [
            label="Cartopy",
            tooltip="Erstellen von Karten und\nAnalyse von Geodaten",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/cartopy/index.html"]
        iris [
            label="Iris",
            tooltip="Visualisierung auf Basis der Climate\nand Forecast (CF) Conventions",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/iris.html"]
        yt [
            label="yt",
            tooltip="Python-Bibliothek zur Analyse\nund Visualisierung von Volumendaten",
            color="#BF80FF",
            target="_top",
            href="../matplotlib/yt.html"]
        mpl -- pandas [color="#BF80FF"]
        mpl -- mpl_scatter_density [color="#BF80FF"]
        pandas  -- geopandas [color="#BF80FF"]
        mpl -- geoplot [color="#BF80FF"]
        mpl -- prettymaps [color="#BF80FF"]
        mpl -- seaborn [color="#BF80FF"]
        mpl -- plotnine [color="#BF80FF"]
        mpl -- yellowbrick [color="#BF80FF"]
        networkx -- graphviz [color="#BF80FF;0.5:#cccccc", style="dashed"]
        graphviz -- graph_tool [color="#cccccc;0.5:#cccccc", style="dashed"]
        mpl -- networkx [color="#BF80FF"]
        mpl -- cartopy [color="#BF80FF"]
        iris -- mpl [color="#BF80FF"]
        iris -- cartopy [color="#BF80FF"]
        yt -- mpl [color="#BF80FF"]
        yt -- opengl [color="#BF80FF;0.5:#FF66B3", style="dashed"]
        mpl -- ipympl [color="#BF80FF;0.5:#00FFFF"]
        mpl -- mpl_altair [color="#BF80FF;0.5:#00FF80"]

        // Bokeh
        bokeh [
            label="Bokeh",
            tooltip="Interaktive Python-Bibliothek\nzur Datenvisualisierung\nin modernen Webbrowsern",
            color="#9999FF",
            target="_top",
            href="../bokeh/index.html"]
        vaex [
            label="Vaex",
            tooltip="Python-Bibliothek zur Datenanalyse\nund -visualisierung",
            color="#9999FF",
            target="_top",
            href="https://github.com/vaexio/vaex"]
        holoviews [
            label="HoloViews",
            tooltip="Python-Bibliothek zur Datenanalyse\nund -visualisierung",
            color="#9999FF",
            target="_top",
            href="http://holoviews.org/"]
        hvplot [
            label="hvPlot",
            tooltip="High-level-Plot-API\nauf Basis von HoloViews",
            color="#9999FF",
            target="_top",
            href="../bokeh/integration/holoviews/hvplot/index.html"]
        datashader [
            label="Datashader",
            tooltip="Grafik-Pipeline-System für\naussagekräftige Darstellungen\ngroßer Datensätze",
            color="#9999FF",
            target="_top",
            href="../bokeh/integration/datashader.html"]
        geoviews [
            label="GeoViews",
            tooltip="Analysieren und Visualisieren von\ngeographischen, meterologischen\nund ozeanischen Daten",
            color="#9999FF",
            target="_top",
            href="../bokeh/integration/holoviews/geoviews.html"]
        geoviews -- cartopy [color="#9999FF;0.5:#BF80FF"]
        geoviews -- holoviews [color="#9999FF"]
        geoviews -- geopandas [color="#9999FF;0.5:#BF80FF", style="dashed"]
        vaex -- bokeh [color="#9999FF"]
        holoviews -- bokeh [color="#9999FF"]
        holoviews -- hvplot [color="#9999FF"]
        hvplot -- pandas [color="#9999FF;0.5:#BF80FF"]
        hvplot -- geopandas [color="#9999FF;0.5:#BF80FF"]
        hvplot -- networkx [color="#9999FF;0.5:#BF80FF"]
        datashader -- bokeh [color="#9999FF"]
        networkx -- bokeh [color="#BF80FF;0.5:#9999FF"]
        datashader -- holoviews [color="#9999FF"]
        vaex -- mpl [color="#9999FF;0.5:#BF80FF"]
        vaex -- bqplot [color="#9999FF;0.5:#4da6ff"]
        vaex -- opengl [color="#9999FF;0.5:#FF66B3"]
        holoviews -- mpl [color="#9999FF;0.5:#BF80FF"]
        datashader -- mpl [color="#9999FF;0.5:#BF80FF"]

        // Vega
        vega [
            label="Vega",
            tooltip="Deklarative Sprache für\ninteraktive Visualisierungen",
            color="#00FF80",
            target="_top",
            href="../vega/index.html"]
        vega_light [
            label="Vega-Lite",
            tooltip="High-level-Grammatik für\nkomplexe Vega-Anwendungen",
            color="#00FF80",
            target="_top",
            href="https://github.com/vega/vega-lite"]
        pdvega [
            label="PdVega",
            tooltip="Interaktive Vega-Light-Plots\naus pandas Dataframes",
            color="#00FF80",
            target="_top",
            href="../vega/pdvega/index.html"]
        altair [
            label="Altair",
            tooltip="Deklarative Visualisierung\nin Python",
            color="#00FF80",
            target="_top",
            href="https://altair-viz.github.io/"]
        mpl_altair [
            label="Matplotlib Altair",
            tooltip="Matplotlib-Renderer\nfür Altair",
            color="#00FF80",
            target="_top",
            href="https://matplotlib.org/mpl-altair/"]
        vega -- vega_light [color="#00FF80"]
        vega_light -- altair [color="#00FF80"]
        vega_light -- pdvega [color="#00FF80"]
        pdvega -- pandas [color="#00FF80;0.5:#BF80FF"]
        altair -- mpl_altair [color="#00FF80"]

        // D3.js
        d3js [
            label="D3.js",
            tooltip="Javascript-Bibliothek mit mächtigen\nVisualisierungskomponenten",
            color="#4da6ff",
            target="_top",
            href="../d3js/index.html"]
        bqplot [
            label="bqplot",
            tooltip="Interaktive Plots\nmit D3.js und ipywidgets",
            color="#4da6ff",
            target="_top",
            href="../d3js/bqplot/index.html"]
        d3po [
            label="d3po",
            tooltip="Javascript-Bibliothekt zum\nErstellen von D3.js-Charts",
            color="#4da6ff",
            target="_top",
            href="https://github.com/adamlabadorf/d3po"]
        plotly [
            label="plotly",
            tooltip="Interaktive Graphikbibliothek\nfür Python",
            color="#4da6ff",
            target="_top",
            href="https://github.com/plotly/plotly.py"]
        d3js -- bqplot [color="#4da6ff"]
        d3js -- plotly [color="#4da6ff"]
        d3js -- d3po [color="#4da6ff"]
        d3js -- vega [color="#4da6ff;0.5:#00FF80"]
        d3js -- javascript [color="#4da6ff;0.5:#00FFFF"]

        // Javascript
        javascript [
            label="Javascript",
            tooltip="Skriptsprache, die ursprünglich für\ndynamisches HTML in Webbrowsern\nentwickelt wurde",
            color="#00FFFF",
            target="_top",
            href="../js/index.html"]
        pythreejs [
            label="pythreejs",
            tooltip="Notebook-Extension\nfür WebGL-fähige Webbrowser",
            color="#00FFFF",
            target="_top",
            href="../js/pythreejs.html"]
        ipyvolume [
            label="IPyvolume",
            tooltip="Python-Bibliothek zur\nVisualisierung von\nVolumen und -Glyphen",
            color="#00FFFF",
            target="_top",
            href="../js/ipyvolume.html"]
        toyplot [
            label="Toyplot",
            tooltip="Leichtgewichtige Bibliothek\nfür ästhetische Plots",
            color="#00FFFF",
            target="_top",
            href="https://toyplot.readthedocs.io/"]
        ipyleaflet [
            label="ipyleaflet",
            tooltip="Interaktive Karten für\nJupyter Notebooks",
            color="#00FFFF",
            target="_top",
            href="../js/ipyleaflet.html"]
        xarray_leaflet [
            label="xarray-leaflet",
            tooltip="xarray extension für Kartendarstellungen",
            color="#00FFFF",
            target="_top",
            href="../js/xarray-leaflet.html"]
        ipympl [
            label="ipympl",
            tooltip="Matplotlib\nJupyter Extension",
            color="#00FFFF",
            target="_top",
            href="https://jupyter-tutorial.readthedocs.io/de/latest/ipywidgets/libs/ipympl.html"]
        javascript -- ipyvolume [color="#00FFFF"]
        javascript -- ipyleaflet [color="#00FFFF"]
        ipyleaflet -- xarray_leaflet [color="#00FFFF"]
        javascript -- ipympl [color="#00FFFF"]
        javascript -- toyplot [color="#00FFFF"]
        javascript -- bokeh [color="#00FFFF;0.5:#9999FF"]
        javascript -- pythreejs [color="#00FFFF"]
    }

Im Folgenden findet ihr tabellarische Übersichten über die verschiedenen
Python-Bibliotheken zur Datenvisualisierung, ihre Aktivitäten und Lizenzen, so
dass ihr einen ersten Anhaltspunkt erhalten könnt, ob die Bibliotheken euren
Anforderungen entspricht.

.. seealso::
   :doc:`python4datascience:productive/licensing`

.. _core-libs:

Zentrale Bibliotheken
---------------------

.. csv-table:: GitHub-Insights: Zentrale Bibliotheken
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Matplotlib <https://github.com/matplotlib/matplotlib>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/contributors/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/license/matplotlib/matplotlib"
    "`bokeh <https://github.com/bokeh/bokeh>`_",".. image:: https://raster.shields.io/github/stars/bokeh/bokeh",".. image:: https://raster.shields.io/github/contributors/bokeh/bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/bokeh/bokeh",".. image:: https://raster.shields.io/github/license/bokeh/bokeh"
    "`plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"

.. _pandas-plot-api:

pandas ``.plot()``-API
----------------------

.. csv-table:: GitHub-Insights: pandas ``.plot()``-API
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`pandas <https://github.com/pandas-dev/pandas>`_",".. image:: https://raster.shields.io/github/stars/pandas-dev/pandas",".. image:: https://raster.shields.io/github/contributors/pandas-dev/pandas",".. image:: https://raster.shields.io/github/commit-activity/y/pandas-dev/pandas",".. image:: https://raster.shields.io/github/license/pandas-dev/pandas"
    "`xarray <https://github.com/pydata/xarray>`_",".. image:: https://raster.shields.io/github/stars/pydata/xarray",".. image:: https://raster.shields.io/github/contributors/pydata/xarray",".. image:: https://raster.shields.io/github/commit-activity/y/pydata/xarray",".. image:: https://raster.shields.io/github/license/pydata/xarray"
    "`Pandas-Bokeh <https://github.com/PatrikHlobil/Pandas-Bokeh>`_",".. image:: https://raster.shields.io/github/stars/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/contributors/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/license/PatrikHlobil/Pandas-Bokeh"
    "`hvplot <https://github.com/holoviz/hvplot>`__",".. image:: https://raster.shields.io/github/stars/holoviz/hvplot",".. image:: https://raster.shields.io/github/contributors/holoviz/hvplot",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/hvplot",".. image:: https://raster.shields.io/github/license/holoviz/hvplot"

.. _further-high-level-apis:

Weitere High-Level-APIs
-----------------------

.. csv-table:: GitHub-Insights: Weitere High-Level-APIs
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`seaborn <https://github.com/mwaskom/seaborn>`_",".. image:: https://raster.shields.io/github/stars/mwaskom/seaborn",".. image:: https://raster.shields.io/github/contributors/mwaskom/seaborn",".. image:: https://raster.shields.io/github/commit-activity/y/mwaskom/seaborn",".. image:: https://raster.shields.io/github/license/mwaskom/seaborn"
    "`altair <https://github.com/altair-viz/altair>`__",".. image:: https://raster.shields.io/github/stars/altair-viz/altair",".. image:: https://raster.shields.io/github/contributors/altair-viz/altair",".. image:: https://raster.shields.io/github/commit-activity/y/altair-viz/altair",".. image:: https://raster.shields.io/github/license/altair-viz/altair"
    "`perspective <https://github.com/finos/perspective>`__",".. image:: https://raster.shields.io/github/stars/finos/perspective",".. image:: https://raster.shields.io/github/contributors/finos/perspective",".. image:: https://raster.shields.io/github/commit-activity/y/finos/perspective",".. image:: https://raster.shields.io/github/license/finos/perspective"
    "`plotnine <https://github.com/has2k1/plotnine>`_",".. image:: https://raster.shields.io/github/stars/has2k1/plotnine",".. image:: https://raster.shields.io/github/contributors/has2k1/plotnine",".. image:: https://raster.shields.io/github/commit-activity/y/has2k1/plotnine",".. image:: https://raster.shields.io/github/license/has2k1/plotnine"
    "`bqplot <https://github.com/bqplot/bqplot>`_",".. image:: https://raster.shields.io/github/stars/bqplot/bqplot",".. image:: https://raster.shields.io/github/contributors/bqplot/bqplot",".. image:: https://raster.shields.io/github/commit-activity/y/bqplot/bqplot",".. image:: https://raster.shields.io/github/license/bqplot/bqplot"
    "`chartify <https://github.com/spotify/chartify>`__",".. image:: https://raster.shields.io/github/stars/spotify/chartify",".. image:: https://raster.shields.io/github/contributors/spotify/chartify",".. image:: https://raster.shields.io/github/commit-activity/y/spotify/chartify",".. image:: https://raster.shields.io/github/license/spotify/chartify"
    "`holoviews <https://github.com/holoviz/holoviews>`__",".. image:: https://raster.shields.io/github/stars/holoviz/holoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/holoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/holoviews",".. image:: https://raster.shields.io/github/license/holoviz/holoviews"
    "`vega <https://github.com/vega/vega>`_",".. image:: https://raster.shields.io/github/stars/vega/vega",".. image:: https://raster.shields.io/github/contributors/vega/vega",".. image:: https://raster.shields.io/github/commit-activity/y/vega/vega",".. image:: https://raster.shields.io/github/license/vega/vega"
    "`Vega-Lite <https://github.com/vega/vega-lite>`_",".. image:: https://raster.shields.io/github/stars/vega/vega-lite",".. image:: https://raster.shields.io/github/contributors/vega/vega-lite",".. image:: https://raster.shields.io/github/commit-activity/y/vega/vega-lite",".. image:: https://raster.shields.io/github/license/vega/vega-lite"
    "`AutoViz <https://github.com/AutoViML/AutoViz>`_",".. image:: https://raster.shields.io/github/stars/AutoViML/AutoViz",".. image:: https://raster.shields.io/github/contributors/AutoViML/AutoViz",".. image:: https://raster.shields.io/github/commit-activity/y/AutoViML/AutoViz",".. image:: https://raster.shields.io/github/license/AutoViML/AutoViz"
    "`Lets-Plot <https://github.com/JetBrains/lets-plot>`__",".. image:: https://raster.shields.io/github/stars/JetBrains/lets-plot",".. image:: https://raster.shields.io/github/contributors/JetBrains/lets-plot",".. image:: https://raster.shields.io/github/commit-activity/y/JetBrains/lets-plot",".. image:: https://raster.shields.io/github/license/JetBrains/lets-plot"
    "`proplot <https://github.com/proplot-dev/proplot>`__",".. image:: https://raster.shields.io/github/stars/proplot-dev/proplot",".. image:: https://raster.shields.io/github/contributors/proplot-dev/proplot",".. image:: https://raster.shields.io/github/commit-activity/y/proplot-dev/proplot",".. image:: https://raster.shields.io/github/license/proplot-dev/proplot"
    "`ipyvizzu <https://github.com/vizzuhq/ipyvizzu>`__",".. image:: https://raster.shields.io/github/stars/vizzuhq/ipyvizzu",".. image:: https://raster.shields.io/github/contributors/vizzuhq/ipyvizzu",".. image:: https://raster.shields.io/github/commit-activity/y/vizzuhq/ipyvizzu",".. image:: https://raster.shields.io/github/license/vizzuhq/ipyvizzu"
    "`ipyvizzu-story <https://github.com/vizzuhq/ipyvizzu-story>`__",".. image:: https://raster.shields.io/github/stars/vizzuhq/ipyvizzu-story",".. image:: https://raster.shields.io/github/contributors/vizzuhq/ipyvizzu-story",".. image:: https://raster.shields.io/github/commit-activity/y/vizzuhq/ipyvizzu-story",".. image:: https://raster.shields.io/github/license/vizzuhq/ipyvizzu-story"
    "`toyplot <https://github.com/sandialabs/toyplot>`_",".. image:: https://raster.shields.io/github/stars/sandialabs/toyplot",".. image:: https://raster.shields.io/github/contributors/sandialabs/toyplot",".. image:: https://raster.shields.io/github/commit-activity/y/sandialabs/toyplot",".. image:: https://raster.shields.io/github/license/sandialabs/toyplot"
    "`quibbler <https://github.com/sandialabs/Technion-Kishony-lab/quibbler>`_",".. image:: https://raster.shields.io/github/stars/Technion-Kishony-lab/quibbler",".. image:: https://raster.shields.io/github/contributors/Technion-Kishony-lab/quibbler",".. image:: https://raster.shields.io/github/commit-activity/y/Technion-Kishony-lab/quibbler",".. image:: https://raster.shields.io/github/license/Technion-Kishony-lab/quibbler"
    "`omniplot <https://github.com/sandialabs/koonimaru/omniplot>`_",".. image:: https://raster.shields.io/github/stars/koonimaru/omniplot",".. image:: https://raster.shields.io/github/contributors/koonimaru/omniplot",".. image:: https://raster.shields.io/github/commit-activity/y/koonimaru/omniplot",".. image:: https://raster.shields.io/github/license/koonimaru/omniplot"

.. _big-data:

Rendern großer Datenmengen
--------------------------

Die Architektur und die zugrundeliegende Technologie für jede Bibliothek
bestimmen die unterstützten Datengrößen und somit, ob die Bibliothek für
mehrdimensionale Arrays, lange Zeitreihen oder andere große Datasets geeignet
ist:

OpenGL-basierte Bibliotheken
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sie können :abbr:`i.A. (im Allgemeinen)` sehr große Datensätze (mehrere
Gigabyte) verarbeiten.

.. csv-table:: GitHub-Insights: OpenGL-basierte Bibliotheken
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`VisPy <https://github.com/vispy/vispy>`_",".. image:: https://raster.shields.io/github/stars/vispy/vispy",".. image:: https://raster.shields.io/github/contributors/vispy/vispy",".. image:: https://raster.shields.io/github/commit-activity/y/vispy/vispy",".. image:: https://raster.shields.io/github/license/vispy/vispy"
    "`vedo <https://github.com/marcomusy/vedo>`_",".. image:: https://raster.shields.io/github/stars/marcomusy/vedo",".. image:: https://raster.shields.io/github/contributors/marcomusy/vedo",".. image:: https://raster.shields.io/github/commit-activity/y/marcomusy/vedo",".. image:: https://raster.shields.io/github/license/marcomusy/vedo"
    "`Polyscope <https://github.com/nmwsharp/polyscope>`_",".. image:: https://raster.shields.io/github/stars/nmwsharp/polyscope",".. image:: https://raster.shields.io/github/contributors/nmwsharp/polyscope",".. image:: https://raster.shields.io/github/commit-activity/y/nmwsharp/polyscope",".. image:: https://raster.shields.io/github/license/nmwsharp/polyscope"
    "`Mayavi <https://github.com/enthought/mayavi>`_",".. image:: https://raster.shields.io/github/stars/enthought/mayavi",".. image:: https://raster.shields.io/github/contributors/enthought/mayavi",".. image:: https://raster.shields.io/github/commit-activity/y/enthought/mayavi",".. image:: https://raster.shields.io/github/license/enthought/mayavi"
    "`Glumpy <https://github.com/glumpy/glumpy>`_",".. image:: https://raster.shields.io/github/stars/glumpy/glumpy",".. image:: https://raster.shields.io/github/contributors/glumpy/glumpy",".. image:: https://raster.shields.io/github/commit-activity/y/glumpy/glumpy",".. image:: https://raster.shields.io/github/license/glumpy/glumpy"
    "`itkwidgets <https://github.com/InsightSoftwareConsortium/itkwidgets>`_",".. image:: https://raster.shields.io/github/stars/InsightSoftwareConsortium/itkwidgets",".. image:: https://raster.shields.io/github/contributors/InsightSoftwareConsortium/itkwidgets",".. image:: https://raster.shields.io/github/commit-activity/y/InsightSoftwareConsortium/itkwidgets",".. image:: https://raster.shields.io/github/license/InsightSoftwareConsortium/itkwidgets"

Matplotlib-basierte Bibliotheken
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sie können :abbr:`i.d.R. (in der Regel)` Hunderttausende von Punkten mit
angemessener Leistung verarbeiten oder in bestimmten Sonderfällen (:abbr:`z.B.
(zum Beispiel)` abhängig vom :doc:`Backend <matplotlib/mpl-backends>`) mehr.

.. csv-table:: GitHub-Insights: Matplotlib-basierte Bibliotheken
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`mpl-scatter-density <https://github.com/astrofrog/mpl-scatter-density>`_",".. image:: https://raster.shields.io/github/stars/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/contributors/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/commit-activity/y/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/license/astrofrog/mpl-scatter-density"

Javascript-basierte Bibliotheken
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sie sind ohne besondere Behandlung beschränkt auf einige tausend bis
hunderttausend Punkte. :doc:`jupyter-tutorial:ipywidgets/index`,
:doc:`bokeh/index` und `Plotly <https://github.com/plotly/plotly.py>`_ nutzen
statt :doc:`python4datascience:data-processing/serialisation-formats/json/index`
jedoch spezielle Transportmechanismen für Binärdaten, sodass sie hunderttausende
bis Millionen von Datenpunkten verarbeiten können. Andere Bibliotheken wie
:doc:`js/ipyvolume`, `Plotly <https://github.com/plotly/plotly.py>`_ und in
einigen Fällen :doc:`bokeh/index` nutzen `WebGL
<https://www.khronos.org/webgl/wiki/Main_Page>`_, sodass sie bis zu einer
Millionen Datenpunkte verarbeiten können.

.. csv-table:: GitHub-Insights: WebGL-basierte Bibliotheken
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Bokeh <https://github.com/bokeh/bokeh>`_",".. image:: https://raster.shields.io/github/stars/bokeh/bokeh",".. image:: https://raster.shields.io/github/contributors/bokeh/bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/bokeh/bokeh",".. image:: https://raster.shields.io/github/license/bokeh/bokeh"
    "`Plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"
    "`pythreejs <https://github.com/jupyter-widgets/pythreejs>`_",".. image:: https://raster.shields.io/github/stars/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/contributors/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/commit-activity/y/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/license/jupyter-widgets/pythreejs"
    "`jupyter-scatter <https://github.com/flekschas/jupyter-scatter>`_",".. image:: https://raster.shields.io/github/stars/flekschas/jupyter-scatter",".. image:: https://raster.shields.io/github/contributors/flekschas/jupyter-scatter",".. image:: https://raster.shields.io/github/commit-activity/y/flekschas/jupyter-scatter",".. image:: https://raster.shields.io/github/license/flekschas/jupyter-scatter"

Server-side Rendering
~~~~~~~~~~~~~~~~~~~~~

:doc:`bokeh/integration/datashader` oder `Vaex
<https://github.com/vaexio/vaex>`_ ermöglichen Milliarden, Billionen oder mehr
Datenpunkte.

.. csv-table:: GitHub-Insights: Server-side Rendering
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`vaex <https://github.com/vaexio/vaex>`_",".. image:: https://raster.shields.io/github/stars/vaexio/vaex",".. image:: https://raster.shields.io/github/contributors/vaexio/vaex",".. image:: https://raster.shields.io/github/commit-activity/y/vaexio/vaex",".. image:: https://raster.shields.io/github/license/vaexio/vaex"
    "`datashader <https://github.com/holoviz/datashader>`_",".. image:: https://raster.shields.io/github/stars/holoviz/datashader",".. image:: https://raster.shields.io/github/contributors/holoviz/datashader",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/datashader",".. image:: https://raster.shields.io/github/license/holoviz/datashader"

Weitere Bibliotheken
--------------------

.. csv-table:: GitHub-Insights: Weitere Bibliotheken
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Facets <https://github.com/PAIR-code/facets>`_",".. image:: https://raster.shields.io/github/stars/PAIR-code/facets",".. image:: https://raster.shields.io/github/contributors/PAIR-code/facets",".. image:: https://raster.shields.io/github/commit-activity/y/PAIR-code/facets",".. image:: https://raster.shields.io/github/license/PAIR-code/facets"
    "`scikit-image <https://github.com/scikit-image/scikit-image/>`_",".. image:: https://raster.shields.io/github/stars/scikit-image/scikit-image",".. image:: https://raster.shields.io/github/contributors/scikit-image/scikit-image",".. image:: https://raster.shields.io/github/commit-activity/y/scikit-image/scikit-image",".. image:: https://raster.shields.io/github/license/scikit-image/scikit-image"
    "`Yellowbrick <https://github.com/DistrictDataLabs/yellowbrick/>`_",".. image:: https://raster.shields.io/github/stars/DistrictDataLabs/yellowbrick",".. image:: https://raster.shields.io/github/contributors/DistrictDataLabs/yellowbrick",".. image:: https://raster.shields.io/github/commit-activity/y/DistrictDataLabs/yellowbrick",".. image:: https://raster.shields.io/github/license/DistrictDataLabs/yellowbrick"
    "`missingno <https://github.com/ResidentMario/missingno>`_",".. image:: https://raster.shields.io/github/stars/ResidentMario/missingno",".. image:: https://raster.shields.io/github/contributors/ResidentMario/missingno",".. image:: https://raster.shields.io/github/commit-activity/y/ResidentMario/missingno",".. image:: https://raster.shields.io/github/license/ResidentMario/missingno"
    "`napari <https://github.com/napari/napari>`_",".. image:: https://raster.shields.io/github/stars/napari/napari",".. image:: https://raster.shields.io/github/contributors/napari/napari",".. image:: https://raster.shields.io/github/commit-activity/y/napari/napari",".. image:: https://raster.shields.io/github/license/napari/napari"
    "`HyperTools <https://github.com/ContextLab/hypertools>`_",".. image:: https://raster.shields.io/github/stars/ContextLab/hypertools",".. image:: https://raster.shields.io/github/contributors/ContextLab/hypertools",".. image:: https://raster.shields.io/github/commit-activity/y/ContextLab/hypertools",".. image:: https://raster.shields.io/github/license/ContextLab/hypertools"
    "`ipympl <https://github.com/matplotlib/ipympl>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/ipympl",".. image:: https://raster.shields.io/github/contributors/matplotlib/ipympl",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/ipympl",".. image:: https://raster.shields.io/github/license/matplotlib/ipympl"
    "`ArviZ <https://github.com/arviz-devs/arviz>`_",".. image:: https://raster.shields.io/github/stars/arviz-devs/arviz",".. image:: https://raster.shields.io/github/contributors/arviz-devs/arviz",".. image:: https://raster.shields.io/github/commit-activity/y/arviz-devs/arviz",".. image:: https://raster.shields.io/github/license/arviz-devs/arviz"
    "`MetPy <https://github.com/Unidata/MetPy>`_",".. image:: https://raster.shields.io/github/stars/Unidata/MetPy",".. image:: https://raster.shields.io/github/contributors/Unidata/MetPy",".. image:: https://raster.shields.io/github/commit-activity/y/Unidata/MetPy",".. image:: https://raster.shields.io/github/license/Unidata/MetPy"
    "`iris <https://github.com/SciTools/iris>`_",".. image:: https://raster.shields.io/github/stars/SciTools/iris",".. image:: https://raster.shields.io/github/contributors/SciTools/iris",".. image:: https://raster.shields.io/github/commit-activity/y/SciTools/iris",".. image:: https://raster.shields.io/github/license/SciTools/iris"
    "`yt <https://github.com/yt-project/yt>`_",".. image:: https://raster.shields.io/github/stars/yt-project/yt",".. image:: https://raster.shields.io/github/contributors/yt-project/yt",".. image:: https://raster.shields.io/github/commit-activity/y/yt-project/yt",".. image:: https://raster.shields.io/github/license/yt-project/yt"

Farbkarten
----------

.. csv-table:: GitHub-Insights: Farbkarten
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`palettable <https://github.com/jiffyclub/palettable>`_",".. image:: https://raster.shields.io/github/stars/jiffyclub/palettable",".. image:: https://raster.shields.io/github/contributors/jiffyclub/palettable",".. image:: https://raster.shields.io/github/commit-activity/y/jiffyclub/palettable",".. image:: https://raster.shields.io/github/license/jiffyclub/palettable"
    "`colorcet <https://github.com/holoviz/colorcet>`_",".. image:: https://raster.shields.io/github/stars/holoviz/colorcet",".. image:: https://raster.shields.io/github/contributors/holoviz/colorcet",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/colorcet",".. image:: https://raster.shields.io/github/license/holoviz/colorcet"
    "`CMasher <https://github.com/1313e/CMasher>`_",".. image:: https://raster.shields.io/github/stars/1313e/CMasher",".. image:: https://raster.shields.io/github/contributors/1313e/CMasher",".. image:: https://raster.shields.io/github/commit-activity/y/1313e/CMasher",".. image:: https://raster.shields.io/github/license/1313e/CMasher"
    "`cmocean <https://github.com/matplotlib/cmocean>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/cmocean",".. image:: https://raster.shields.io/github/contributors/matplotlib/cmocean",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/cmocean",".. image:: https://raster.shields.io/github/license/matplotlib/cmocean"
    "`distinctipy <https://github.com/alan-turing-institute/distinctipy>`_",".. image:: https://raster.shields.io/github/stars/alan-turing-institute/distinctipy",".. image:: https://raster.shields.io/github/contributors/alan-turing-institute/distinctipy",".. image:: https://raster.shields.io/github/commit-activity/y/alan-turing-institute/distinctipy",".. image:: https://raster.shields.io/github/license/alan-turing-institute/distinctipy"
    "`viscm <https://github.com/matplotlib/viscm>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/viscm",".. image:: https://raster.shields.io/github/contributors/matplotlib/viscm",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/viscm",".. image:: https://raster.shields.io/github/license/matplotlib/viscm"
    "`cmcrameri <https://github.com/callumrollo/cmcrameri>`_",".. image:: https://raster.shields.io/github/stars/callumrollo/cmcrameri",".. image:: https://raster.shields.io/github/contributors/callumrollo/cmcrameri",".. image:: https://raster.shields.io/github/commit-activity/y/callumrollo/cmcrameri",".. image:: https://raster.shields.io/github/license/callumrollo/cmcrameri"

.. _chart-types:

Diagrammtypen
-------------

Statistische Darstellungen
~~~~~~~~~~~~~~~~~~~~~~~~~~

Streudiagramme, Linien, Flächen, Balken, Histogramme

.. csv-table:: GitHub-Insights: Statistische Darstellungen
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`seaborn <https://github.com/mwaskom/seaborn>`_",".. image:: https://raster.shields.io/github/stars/mwaskom/seaborn",".. image:: https://raster.shields.io/github/contributors/mwaskom/seaborn",".. image:: https://raster.shields.io/github/commit-activity/y/mwaskom/seaborn",".. image:: https://raster.shields.io/github/license/mwaskom/seaborn"
    "`bqplot <https://github.com/bqplot/bqplot>`_",".. image:: https://raster.shields.io/github/stars/bqplot/bqplot",".. image:: https://raster.shields.io/github/contributors/bqplot/bqplot",".. image:: https://raster.shields.io/github/commit-activity/y/bqplot/bqplot",".. image:: https://raster.shields.io/github/license/bqplot/bqplot"
    "`Matplotlib Altair <https://github.com/matplotlib/mpl-altair>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/contributors/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/license/matplotlib/mpl-altair"

Regelmäßige Gitter mit rechteckigen Maschen
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. csv-table:: GitHub-Insights: Regelmäßige Gitter mit rechteckigen Maschen
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Matplotlib <https://github.com/matplotlib/matplotlib>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/contributors/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/license/matplotlib/matplotlib"
    "`bokeh <https://github.com/bokeh/bokeh>`_",".. image:: https://raster.shields.io/github/stars/bokeh/bokeh",".. image:: https://raster.shields.io/github/contributors/bokeh/bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/bokeh/bokeh",".. image:: https://raster.shields.io/github/license/bokeh/bokeh"
    "`Plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"
    "`datashader <https://github.com/holoviz/datashader>`_",".. image:: https://raster.shields.io/github/stars/holoviz/datashader",".. image:: https://raster.shields.io/github/contributors/holoviz/datashader",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/datashader",".. image:: https://raster.shields.io/github/license/holoviz/datashader"
    "`HoloViews <https://github.com/holoviz/holoviews>`_",".. image:: https://raster.shields.io/github/stars/holoviz/holoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/holoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/holoviews",".. image:: https://raster.shields.io/github/license/holoviz/holoviews"

Unregelmäßige 2D-Netze (Dreiecksgitter)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. csv-table:: GitHub-Insights: Unregelmäßige 2D-Netze (Dreiecksgitter)
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Matplotlib <https://github.com/matplotlib/matplotlib>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/contributors/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/license/matplotlib/matplotlib"
    "`bokeh <https://github.com/bokeh/bokeh>`_",".. image:: https://raster.shields.io/github/stars/bokeh/bokeh",".. image:: https://raster.shields.io/github/contributors/bokeh/bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/bokeh/bokeh",".. image:: https://raster.shields.io/github/license/bokeh/bokeh"
    "`datashader <https://github.com/holoviz/datashader>`_",".. image:: https://raster.shields.io/github/stars/holoviz/datashader",".. image:: https://raster.shields.io/github/contributors/holoviz/datashader",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/datashader",".. image:: https://raster.shields.io/github/license/holoviz/datashader"
    "`HoloViews <https://github.com/holoviz/holoviews>`_",".. image:: https://raster.shields.io/github/stars/holoviz/holoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/holoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/holoviews",".. image:: https://raster.shields.io/github/license/holoviz/holoviews"

Geographie
~~~~~~~~~~

.. csv-table:: GitHub-Insights: Geographie
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"
    "`prettymaps <https://github.com/marceloprates/prettymaps>`__",".. image:: https://raster.shields.io/github/stars/marceloprates/prettymaps",".. image:: https://raster.shields.io/github/contributors/marceloprates/prettymaps",".. image:: https://raster.shields.io/github/commit-activity/y/marceloprates/prettymaps",".. image:: https://raster.shields.io/github/license/marceloprates/prettymaps"
    "`kepler.gl <https://github.com/keplergl/kepler.gl>`__",".. image:: https://raster.shields.io/github/stars/keplergl/kepler.gl",".. image:: https://raster.shields.io/github/contributors/keplergl/kepler.gl",".. image:: https://raster.shields.io/github/commit-activity/y/keplergl/kepler.gl",".. image:: https://raster.shields.io/github/license/keplergl/kepler.gl"
    "`folium <https://github.com/python-visualization/folium>`__",".. image:: https://raster.shields.io/github/stars/python-visualization/folium",".. image:: https://raster.shields.io/github/contributors/python-visualization/folium",".. image:: https://raster.shields.io/github/commit-activity/y/python-visualization/folium",".. image:: https://raster.shields.io/github/license/python-visualization/folium"
    "`OSMnx <https://github.com/gboeing/osmnx>`_",".. image:: https://raster.shields.io/github/stars/gboeing/osmnx",".. image:: https://raster.shields.io/github/contributors/gboeing/osmnx",".. image:: https://raster.shields.io/github/commit-activity/y/gboeing/osmnx",".. image:: https://raster.shields.io/github/license/gboeing/osmnx"
    "`geopandas <https://github.com/geopandas/geopandas>`_",".. image:: https://raster.shields.io/github/stars/geopandas/geopandas",".. image:: https://raster.shields.io/github/contributors/geopandas/geopandas",".. image:: https://raster.shields.io/github/commit-activity/y/geopandas/geopandas",".. image:: https://raster.shields.io/github/license/geopandas/geopandas"
    "`datashader <https://github.com/holoviz/datashader>`_",".. image:: https://raster.shields.io/github/stars/holoviz/datashader",".. image:: https://raster.shields.io/github/contributors/holoviz/datashader",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/datashader",".. image:: https://raster.shields.io/github/license/holoviz/datashader"
    "`geemap <https://github.com/gee-community/geemap>`_",".. image:: https://raster.shields.io/github/stars/gee-community/geemap",".. image:: https://raster.shields.io/github/contributors/gee-community/geemap",".. image:: https://raster.shields.io/github/commit-activity/y/gee-community/geemap",".. image:: https://raster.shields.io/github/license/gee-community/geemap"
    "`leafmap <https://github.com/opengeos/leafmap>`_",".. image:: https://raster.shields.io/github/stars/opengeos/leafmap",".. image:: https://raster.shields.io/github/contributors/opengeos/leafmap",".. image:: https://raster.shields.io/github/commit-activity/y/opengeos/leafmap",".. image:: https://raster.shields.io/github/license/opengeos/leafmap"
    "`ipyleaflet <https://github.com/jupyter-widgets/ipyleaflet>`_",".. image:: https://raster.shields.io/github/stars/jupyter-widgets/ipyleaflet",".. image:: https://raster.shields.io/github/contributors/jupyter-widgets/ipyleaflet",".. image:: https://raster.shields.io/github/commit-activity/y/jupyter-widgets/ipyleaflet",".. image:: https://raster.shields.io/github/license/jupyter-widgets/ipyleaflet"
    "`cartopy <https://github.com/SciTools/cartopy>`_",".. image:: https://raster.shields.io/github/stars/SciTools/cartopy",".. image:: https://raster.shields.io/github/contributors/SciTools/cartopy",".. image:: https://raster.shields.io/github/commit-activity/y/SciTools/cartopy",".. image:: https://raster.shields.io/github/license/SciTools/cartopy"
    "`geoplot <https://github.com/ResidentMario/geoplot/>`__",".. image:: https://raster.shields.io/github/stars/ResidentMario/geoplot",".. image:: https://raster.shields.io/github/contributors/ResidentMario/geoplot",".. image:: https://raster.shields.io/github/commit-activity/y/ResidentMario/geoplot",".. image:: https://raster.shields.io/github/license/ResidentMario/geoplot"
    "`PyGMT <https://github.com/GenericMappingTools/pygmt>`__",".. image:: https://raster.shields.io/github/stars/GenericMappingTools/pygmt",".. image:: https://raster.shields.io/github/contributors/GenericMappingTools/pygmt",".. image:: https://raster.shields.io/github/commit-activity/y/GenericMappingTools/pygmt",".. image:: https://raster.shields.io/github/license/GenericMappingTools/pygmt"
    "`GeoViews <https://github.com/holoviz/geoviews>`_",".. image:: https://raster.shields.io/github/stars/holoviz/geoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/geoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/geoviews",".. image:: https://raster.shields.io/github/license/holoviz/geoviews"
    "`Pyrosm <https://github.com/HTenkanen/pyrosm>`_",".. image:: https://raster.shields.io/github/stars/HTenkanen/pyrosm",".. image:: https://raster.shields.io/github/contributors/HTenkanen/pyrosm",".. image:: https://raster.shields.io/github/commit-activity/y/HTenkanen/pyrosm",".. image:: https://raster.shields.io/github/license/HTenkanen/pyrosm"
    "`EOmaps <https://github.com/raphaelquast/eomaps>`_",".. image:: https://raster.shields.io/github/stars/raphaelquast/eomaps",".. image:: https://raster.shields.io/github/contributors/raphaelquast/eomaps",".. image:: https://raster.shields.io/github/commit-activity/y/raphaelquast/eomaps",".. image:: https://raster.shields.io/github/license/raphaelquast/eomaps"
    "`mapwidget <https://github.com/opengeos/mapwidget>`_",".. image:: https://raster.shields.io/github/stars/opengeos/mapwidget",".. image:: https://raster.shields.io/github/contributors/opengeos/mapwidget",".. image:: https://raster.shields.io/github/commit-activity/y/opengeos/mapwidget",".. image:: https://raster.shields.io/github/license/opengeos/mapwidget"
    "`splot <https://github.com/pysal/splot>`_",".. image:: https://raster.shields.io/github/stars/pysal/splot",".. image:: https://raster.shields.io/github/contributors/pysal/splot",".. image:: https://raster.shields.io/github/commit-activity/y/pysal/splot",".. image:: https://raster.shields.io/github/license/pysal/splot"
    "`Gspatial Plot <https://github.com/ambeelabs/gspatial_plot>`_",".. image:: https://raster.shields.io/github/stars/ambeelabs/gspatial_plot",".. image:: https://raster.shields.io/github/contributors/ambeelabs/gspatial_plot",".. image:: https://raster.shields.io/github/commit-activity/y/ambeelabs/gspatial_plot",".. image:: https://raster.shields.io/github/license/ambeelabs/gspatial_plot"
    "`xarray-leaflet <https://github.com/davidbrochart/xarray_leaflet>`_",".. image:: https://raster.shields.io/github/stars/davidbrochart/xarray_leaflet",".. image:: https://raster.shields.io/github/contributors/davidbrochart/xarray_leaflet",".. image:: https://raster.shields.io/github/commit-activity/y/davidbrochart/xarray_leaflet",".. image:: https://raster.shields.io/github/license/davidbrochart/xarray_leaflet"

Graphen und Netzwerke
~~~~~~~~~~~~~~~~~~~~~

.. csv-table:: GitHub-Insights: Graphen und Netzwerke
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"
    "`networkx <https://github.com/networkx/networkx>`_",".. image:: https://raster.shields.io/github/stars/networkx/networkx",".. image:: https://raster.shields.io/github/contributors/networkx/networkx",".. image:: https://raster.shields.io/github/commit-activity/y/networkx/networkx",".. image:: https://raster.shields.io/github/license/networkx/networkx"
    "`datashader <https://github.com/holoviz/datashader>`_",".. image:: https://raster.shields.io/github/stars/holoviz/datashader",".. image:: https://raster.shields.io/github/contributors/holoviz/datashader",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/datashader",".. image:: https://raster.shields.io/github/license/holoviz/datashader"
    "`HoloViews <https://github.com/holoviz/holoviews>`_",".. image:: https://raster.shields.io/github/stars/holoviz/holoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/holoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/holoviews",".. image:: https://raster.shields.io/github/license/holoviz/holoviews"
    "`graphviz <https://github.com/xflr6/graphviz>`_",".. image:: https://raster.shields.io/github/stars/xflr6/graphviz",".. image:: https://raster.shields.io/github/contributors/xflr6/graphviz",".. image:: https://raster.shields.io/github/commit-activity/y/xflr6/graphviz",".. image:: https://raster.shields.io/github/license/xflr6/graphviz"
    "`python-igraph <https://github.com/igraph/python-igraph>`_",".. image:: https://raster.shields.io/github/stars/igraph/python-igraph",".. image:: https://raster.shields.io/github/contributors/igraph/python-igraph",".. image:: https://raster.shields.io/github/commit-activity/y/igraph/python-igraph",".. image:: https://raster.shields.io/github/license/igraph/python-igraph"
    "`Pandas-Bokeh <https://github.com/PatrikHlobil/Pandas-Bokeh>`_",".. image:: https://raster.shields.io/github/stars/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/contributors/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/commit-activity/y/PatrikHlobil/Pandas-Bokeh",".. image:: https://raster.shields.io/github/license/PatrikHlobil/Pandas-Bokeh"
    "`pyvis <https://github.com/WestHealth/pyvis>`_",".. image:: https://raster.shields.io/github/stars/WestHealth/pyvis",".. image:: https://raster.shields.io/github/contributors/WestHealth/pyvis",".. image:: https://raster.shields.io/github/commit-activity/y/WestHealth/pyvis",".. image:: https://raster.shields.io/github/license/WestHealth/pyvis"
    "`pydot <https://github.com/pydot/pydot>`_",".. image:: https://raster.shields.io/github/stars/pydot/pydot",".. image:: https://raster.shields.io/github/contributors/pydot/pydot",".. image:: https://raster.shields.io/github/commit-activity/y/pydot/pydot",".. image:: https://raster.shields.io/github/license/pydot/pydot"
    "`PyGraphviz <https://github.com/pygraphviz/pygraphviz>`_",".. image:: https://raster.shields.io/github/stars/pygraphviz/pygraphviz",".. image:: https://raster.shields.io/github/contributors/pygraphviz/pygraphviz",".. image:: https://raster.shields.io/github/commit-activity/y/pygraphviz/pygraphviz",".. image:: https://raster.shields.io/github/license/pygraphviz/pygraphviz"
    "`nxviz <https://github.com/ericmjl/nxviz>`_",".. image:: https://raster.shields.io/github/stars/ericmjl/nxviz",".. image:: https://raster.shields.io/github/contributors/ericmjl/nxviz",".. image:: https://raster.shields.io/github/commit-activity/y/ericmjl/nxviz",".. image:: https://raster.shields.io/github/license/ericmjl/nxviz"
    "`py4cytoscape <https://github.com/cytoscape/py4cytoscape>`_",".. image:: https://raster.shields.io/github/stars/cytoscape/py4cytoscape",".. image:: https://raster.shields.io/github/contributors/cytoscape/py4cytoscape",".. image:: https://raster.shields.io/github/commit-activity/y/cytoscape/py4cytoscape",".. image:: https://raster.shields.io/github/license/cytoscape/py4cytoscape"
    "`ipycytoscape <https://github.com/cytoscape/ipycytoscape>`_",".. image:: https://raster.shields.io/github/stars/cytoscape/ipycytoscape",".. image:: https://raster.shields.io/github/contributors/cytoscape/ipycytoscape",".. image:: https://raster.shields.io/github/commit-activity/y/cytoscape/ipycytoscape",".. image:: https://raster.shields.io/github/license/cytoscape/ipycytoscape"
    "`Py3Plex <https://github.com/SkBlaz/Py3Plex>`_",".. image:: https://raster.shields.io/github/stars/SkBlaz/Py3Plex",".. image:: https://raster.shields.io/github/contributors/SkBlaz/Py3Plex",".. image:: https://raster.shields.io/github/commit-activity/y/SkBlaz/Py3Plex",".. image:: https://raster.shields.io/github/license/SkBlaz/Py3Plex"
    "`ipysigma <https://github.com/medialab/ipysigma>`_",".. image:: https://raster.shields.io/github/stars/medialab/ipysigma",".. image:: https://raster.shields.io/github/contributors/medialab/ipysigma",".. image:: https://raster.shields.io/github/commit-activity/y/medialab/ipysigma",".. image:: https://raster.shields.io/github/license/medialab/ipysigma"
    "`ipydagred3 <https://github.com/timkpaine/ipydagred3>`_",".. image:: https://raster.shields.io/github/stars/timkpaine/ipydagred3",".. image:: https://raster.shields.io/github/contributors/timkpaine/ipydagred3",".. image:: https://raster.shields.io/github/commit-activity/y/timkpaine/ipydagred3",".. image:: https://raster.shields.io/github/license/timkpaine/ipydagred3"

3D-Darstellungen (Netze, Streudiagramme)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. csv-table:: GitHub-Insights: 3D-Darstellungen (Netze, Streudiagramme)
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`Matplotlib <https://github.com/matplotlib/matplotlib>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/contributors/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/matplotlib",".. image:: https://raster.shields.io/github/license/matplotlib/matplotlib"
    "`Plotly <https://github.com/plotly/plotly.py>`_",".. image:: https://raster.shields.io/github/stars/plotly/plotly.py",".. image:: https://raster.shields.io/github/contributors/plotly/plotly.py",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly.py",".. image:: https://raster.shields.io/github/license/plotly/plotly.py"
    "`HoloViews <https://github.com/holoviz/holoviews>`_",".. image:: https://raster.shields.io/github/stars/holoviz/holoviews",".. image:: https://raster.shields.io/github/contributors/holoviz/holoviews",".. image:: https://raster.shields.io/github/commit-activity/y/holoviz/holoviews",".. image:: https://raster.shields.io/github/license/holoviz/holoviews"
    "`ipyvolume <https://github.com/widgetti/ipyvolume>`_",".. image:: https://raster.shields.io/github/stars/widgetti/ipyvolume",".. image:: https://raster.shields.io/github/contributors/widgetti/ipyvolume",".. image:: https://raster.shields.io/github/commit-activity/y/widgetti/ipyvolume",".. image:: https://raster.shields.io/github/license/widgetti/ipyvolume"
    "`pythreejs <https://github.com/jupyter-widgets/pythreejs>`_",".. image:: https://raster.shields.io/github/stars/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/contributors/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/commit-activity/y/jupyter-widgets/pythreejs",".. image:: https://raster.shields.io/github/license/jupyter-widgets/pythreejs"
    "`mpl-scatter-density <https://github.com/astrofrog/mpl-scatter-density>`_",".. image:: https://raster.shields.io/github/stars/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/contributors/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/commit-activity/y/astrofrog/mpl-scatter-density",".. image:: https://raster.shields.io/github/license/astrofrog/mpl-scatter-density"

Ruhende Projekte
----------------

.. csv-table:: GitHub-Insights: Ruhende Projekte (Stand: 18.12.2023)
    :header: "Name", "Stars", "Mitwirkende", "Commit-Aktivität", "Lizenz"

    "`graph-tool <https://github.com/antmd/graph-tool>`_",".. image:: https://raster.shields.io/github/stars/antmd/graph-tool",".. image:: https://raster.shields.io/github/contributors/antmd/graph-tool",".. image:: https://raster.shields.io/github/commit-activity/y/antmd/graph-tool",".. image:: https://raster.shields.io/github/license/antmd/graph-tool"
    "`ggpy <https://github.com/yhat/ggpy>`_",".. image:: https://raster.shields.io/github/stars/yhat/ggpy",".. image:: https://raster.shields.io/github/contributors/yhat/ggpy",".. image:: https://raster.shields.io/github/commit-activity/y/yhat/ggpy",".. image:: https://raster.shields.io/github/license/yhat/ggpy"
    "`cufflinks <https://github.com/santosjorge/cufflinks>`_",".. image:: https://raster.shields.io/github/stars/santosjorge/cufflinks",".. image:: https://raster.shields.io/github/contributors/santosjorge/cufflinks",".. image:: https://raster.shields.io/github/commit-activity/y/santosjorge/cufflinks",".. image:: https://raster.shields.io/github/license/santosjorge/cufflinks"
    "`scikit-plot <https://github.com/reiinakano/scikit-plot>`_",".. image:: https://raster.shields.io/github/stars/reiinakano/scikit-plot",".. image:: https://raster.shields.io/github/contributors/reiinakano/scikit-plot",".. image:: https://raster.shields.io/github/commit-activity/y/reiinakano/scikit-plot",".. image:: https://raster.shields.io/github/license/reiinakano/scikit-plot"
    "`mpld3 <https://github.com/mpld3/mpld3>`_",".. image:: https://raster.shields.io/github/stars/mpld3/mpld3",".. image:: https://raster.shields.io/github/contributors/mpld3/mpld3",".. image:: https://raster.shields.io/github/commit-activity/y/mpld3/mpld3",".. image:: https://raster.shields.io/github/license/mpld3/mpld3"
    "`vincent <https://github.com/wrobstory/vincent>`_",".. image:: https://raster.shields.io/github/stars/wrobstory/vincent",".. image:: https://raster.shields.io/github/contributors/wrobstory/vincent",".. image:: https://raster.shields.io/github/commit-activity/y/wrobstory/vincent",".. image:: https://raster.shields.io/github/license/wrobstory/vincent"
    "`geoplotlib <https://github.com/andrea-cuttone/geoplotlib/>`__",".. image:: https://raster.shields.io/github/stars/andrea-cuttone/geoplotlib",".. image:: https://raster.shields.io/github/contributors/andrea-cuttone/geoplotlib",".. image:: https://raster.shields.io/github/commit-activity/y/andrea-cuttone/geoplotlib",".. image:: https://raster.shields.io/github/license/andrea-cuttone/geoplotlib"
    "`gmplot <https://github.com/gmplot/gmplot>`__",".. image:: https://raster.shields.io/github/stars/gmplot/gmplot",".. image:: https://raster.shields.io/github/contributors/gmplot/gmplot",".. image:: https://raster.shields.io/github/commit-activity/y/gmplot/gmplot",".. image:: https://raster.shields.io/github/license/gmplot/gmplot"
    "`plotly_express <https://github.com/plotly/plotly_express>`__",".. image:: https://raster.shields.io/github/stars/plotly/plotly_express",".. image:: https://raster.shields.io/github/contributors/plotly/plotly_express",".. image:: https://raster.shields.io/github/commit-activity/y/plotly/plotly_express",".. image:: https://raster.shields.io/github/license/plotly/plotly_express"
    "`PyGSP <https://github.com/epfl-lts2/pygsp>`_",".. image:: https://raster.shields.io/github/stars/epfl-lts2/pygsp",".. image:: https://raster.shields.io/github/contributors/epfl-lts2/pygsp",".. image:: https://raster.shields.io/github/commit-activity/y/epfl-lts2/pygsp",".. image:: https://raster.shields.io/github/license/epfl-lts2/pygsp"
    "`PdVega <https://github.com/altair-viz/pdvega>`_",".. image:: https://raster.shields.io/github/stars/altair-viz/pdvega",".. image:: https://raster.shields.io/github/contributors/altair-viz/pdvega",".. image:: https://raster.shields.io/github/commit-activity/y/altair-viz/pdvega",".. image:: https://raster.shields.io/github/license/altair-viz/pdvega"
    "`Clustergrammer2 <https://github.com/ismms-himc/clustergrammer2>`_",".. image:: https://raster.shields.io/github/stars/ismms-himc/clustergrammer2",".. image:: https://raster.shields.io/github/contributors/ismms-himc/clustergrammer2",".. image:: https://raster.shields.io/github/commit-activity/y/ismms-himc/clustergrammer2",".. image:: https://raster.shields.io/github/license/ismms-himc/clustergrammer2"
    "`chart <https://github.com/maxhumber/chart>`_",".. image:: https://raster.shields.io/github/stars/maxhumber/chart",".. image:: https://raster.shields.io/github/contributors/maxhumber/chart",".. image:: https://raster.shields.io/github/commit-activity/y/maxhumber/chart",".. image:: https://raster.shields.io/github/license/maxhumber/chart"
    "`xtrude <https://github.com/davidbrochart/xtrude>`_",".. image:: https://raster.shields.io/github/stars/davidbrochart/xtrude",".. image:: https://raster.shields.io/github/contributors/davidbrochart/xtrude",".. image:: https://raster.shields.io/github/commit-activity/y/davidbrochart/xtrude",".. image:: https://raster.shields.io/github/license/davidbrochart/xtrude"
    "`Matplotlib Altair <https://github.com/matplotlib/mpl-altair>`_",".. image:: https://raster.shields.io/github/stars/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/contributors/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/commit-activity/y/matplotlib/mpl-altair",".. image:: https://raster.shields.io/github/license/matplotlib/mpl-altair"
    "`d3po <https://github.com/adamlabadorf/d3po>`_",".. image:: https://raster.shields.io/github/stars/adamlabadorf/d3po",".. image:: https://raster.shields.io/github/contributors/adamlabadorf/d3po",".. image:: https://raster.shields.io/github/commit-activity/y/adamlabadorf/d3po",".. image:: https://raster.shields.io/github/license/adamlabadorf/d3po"
