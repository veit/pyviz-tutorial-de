Konvertieren
============

.. _tippecanoe:

Tippecanoe
----------

`Tippecanoe <https://github.com/felt/tippecanoe>`__ erstellt Vektorkacheln,
:abbr:`u.a. (unter anderem)` aus `GeoJSON <https://geojson.org>`_- und
`FlatGeobuf <https://github.com/flatgeobuf/flatgeobuf>`_-Dateien. Ab Version
2.17 unterstützt Tippecanoe auch PMTiles mit der Option
:samp:`-o {FILENAME}.pmtiles`. Um mehrere PMTiles-Dateien zu einer einzigen
Datei zusammenzufügen, könnt ihr `tile-join
<https://github.com/felt/tippecanoe?tab=readme-ov-file#tile-join>`_ verwenden,
das mit Tippecanoe mitkommt.

Installation
~~~~~~~~~~~~

.. tab:: Debian/Ubuntu

   .. code-block:: console

      $ sudo apt-get install gcc g++ git make libsqlite3-dev zlib1g-dev
      $ git clone https://github.com/felt/tippecanoe.git
      $ cd tippecanoe
      $ make -j
      $ make install

.. tab:: macOS

   .. code-block:: console

      $ brew install tippecanoe

pmtiles CLI
-----------

Das Kommandozeilentool `pmtiles <https://docs.protomaps.com/pmtiles/cli>`_
konvertiert `MBTiles
<https://www.python4data.science/de/latest/data-processing/geodata.html#mbtiles>`_
in PMTiles mit dem Befehl :samp:`pmtiles convert {INPUT}.mbtiles
{OUTPUT}.pmtiles`.

Installation
~~~~~~~~~~~~

.. code-block:: console

   $ uv add pmtiles

rio-pmtiles
-----------

`rio-pmtiles <https://pypi.org/project/rio-pmtiles/>`_ ist ein Plugin für
`Rasterio <https://rasterio.readthedocs.io/en/stable/>`_, mit dem sich kleine und mittlere Rasterdaten (~1GB) konvertieren lassen.

Installation
~~~~~~~~~~~~

.. code-block:: console

   $ uv add rio-pmtiles

GDAL
----

`GDAL <https://gdal.org/en/stable/>`_ untertützt ab Version 3.8.0 PMTiles. Mit
``ogr2ogr`` lässt sich eine breite Palette von Formaten in PMTiles umwandeln,
:abbr:`z.B. (zum Beispiel)` `Shapefiles
<https://enterprise.arcgis.com/de/portal/latest/use/shapefiles.htm>`_ und
:doc:`python4datascience:data-processing/postgresql/postgis/index`-Tabellen:

.. code-block:: console

   $ ogr2ogr -dsco MINZOOM=10 -dsco MAXZOOM=15 -f "PMTiles" FILENAME.pmtiles MY_SHAPES.shp
   $ ogr2ogr -dsco MINZOOM=0 -dsco MAXZOOM=15 -f "PMTiles" FILENAME.pmtiles "PG:host=MY_HOST port=MY_PORT dbname=MY_DATABASE user=MY_USERNAME password=MY_PASSWORD schemas=MY_SCHEMA"

.. tip::
   ``ogr2ogr`` zur Erstellung von Vektor-PMTiles empfiehlt sich nur für kleinere
   Datensätze: :ref:`tippecanoe` erzeugt wesentlich effizienter
   Übersichtskacheln.

.. seealso::
   * `GDAL documentation
     <https://gdal.org/en/stable/drivers/vector/pmtiles.html>`_

Installation
~~~~~~~~~~~~

.. tab:: Debian/Ubuntu

   .. code-block:: console

      $ sudo apt install libgdal20

.. tab:: macOS

   Die Apache Arrow-Bibliothek der aktuellen Homebrew-Distribution ist defekt.
   Um GDAL erfolgreich zu bauen, konfiguriert CMake so, dass das Arrow-Paket
   nicht gefunden wird. Ebenso wird Boost nicht mehr mit libkml gebündelt,
   weswegen libkml beim Bauen unter MacOS deaktiviert werden sollte:

   .. code-block:: console

      $ cmake -DCMAKE_DISABLE_FIND_PACKAGE_Arrow=ON ..
      $ cmake -DGDAL_USE_LIBKML=OFF ..
      $ brew install gdal

protomaps/basemaps
------------------

Die Protomaps-Basiskarte basiert auf `OpenStreetMap
<https://www.openstreetmap.org/>`_- und `Natural Earth
<https://www.naturalearthdata.com>`_-Daten. Sie enthält nicht alle Daten und
Tags von OSM; stattdessen ist sie so konzipiert, dass sie ein ausgewogenes
Verhältnis zwischen Kachelgröße und Vollständigkeit bietet, um als allgemeine
Kontextkarte verwendet werden zu können.

Die Organisation der Ebenen und Tags ist vom Open-Source-Projekt `Tilezen
<https://tilezen.readthedocs.io/en/latest/layers/>`_ abgeleitet. Der Umfang der
Inhalte und die Auswahl der Daten, die bei bestimmten Zoomstufen einbezogen
werden, spiegeln sich in den Referenzimplementierungen von Tilezen-Stilen wie
`Bubble Wrap <https://tangrams.github.io/bubble-wrap/>`_ wider.

.. seealso::
   * `Basemap Layers
     <https://docs.protomaps.com/basemaps/layers#basemap-layers>`_

Das `basemaps <https://github.com/protomaps/basemaps>`_-Repository enthält in
`tiles <https://github.com/protomaps/basemaps/tree/main/tiles>`_ ein `Planetiler
<https://github.com/onthegomap/planetiler>`_-Profil zur Erzeugung von PMTiles
auf Planetenebene aus OpenStreetMap. Die Layer in diesem Tileset sind unter
`Basemap Layers <https://docs.protomaps.com/basemaps/layers>`__ dokumentiert und
tägliche Builds können kostenlos von `maps.protomaps.com/builds
<https://maps.protomaps.com/builds/>`_ heruntergeladen werden.

Die Pipeline zur Erzeugung dieser täglichen Basiskarte ist `quelloffen
<https://github.com/protomaps/basemaps/tree/main/tiles>`_ und basiert auf der
Planetiler Java Tiling Engine. Sie kann für eure lokale Stadt oder euer Land in
wenigen Minuten ausgeführt werden.

Die Vorteile einer selbst erstellten Basiskarte sind unter anderem:

Aktuelle Basiskarten
    Erstellt Kacheln aus bestimmten OpenStreetMap-Schnappschüssen, :abbr:`z.B.
    (zum Beispiel)` aus den aktuellen Daten von `SliceOSM
    <https://slice.openstreetmap.us/>`_.

Ausschnitte
    Erstellt benutzerdefinierte, fokussierte Gebietskarten. Das Extrahieren
    eines Gebiets aus der täglichen Planetenkarte enthält zusätzliche Daten in
    Kacheln mit niedrigem Zoomfaktor, wie in der folgenden Abbildung zu sehen
    ist:

    .. figure:: basemap.png
       :alt: Basiskarte von Berlin-Reinickendorf

       Basiskarte von Berlin-Reinickendorf

    #. Ihr benötigt eine Java-Laufzeitumgebung ≥21 und Maven:

       .. tab:: Debian/Ubuntu

          .. code-block:: console

             $ apt-install openjdk-21-jdk maven

       .. tab:: macOS

          .. code-block:: console

             $ brew install openjdk maven

    #. Einen OpenStreetMap-Ausschnitt, der euer Interessengebiet abdeckt,
       :abbr:`z.B. (zum Beispiel)` einen On-Demand-Download von `SliceOSM
       <https://slice.openstreetmap.us/>`_ oder einen vorgenerierten Download
       von `Geofabrik Downloads <https://download.geofabrik.de>`_.
    #. Die Bezirksgrenzen von Berlin als GeoJSON-Datei, heruntergeladen von
       `ODIS <https://daten.odis-berlin.de>`_ oder von `Who’s On First Spelunker
       <https://spelunker.whosonfirst.org>`_.
    #. Check-out des basemaps-Projekts und bauen der JAR-Datei:

       .. code-block:: console

          $ git clone https://github.com/protomaps/basemaps
          $ cd basemaps/tiles
          $ mvn clean package

    #. Erzeugt eure Kacheln:

       .. code-block:: console

          $ java -jar  target/protomaps-basemap-HEAD-with-deps.jar --clip='~/reinickendorf.geojson' --area=reinickendorf --download

       Dabei werden auch Ressourcen wie vorverarbeitete OSM-Wasser- und
       Landpolygone, `Natural Earth <https://www.naturalearthdata.com>`_ und
       Datensätze für Sprachunterstützung und Ranking heruntergeladen.

    #. Schließlich könnt ihr euch die neue Karte anzeigen lassen, indem ihr die
       Datei :file:`{REGION}.pntiles` in den `Basemaps Viewer
       <https://maps.protomaps.com/>`_ zieht.

    Eine benutzerdefinierte Karte des gesamten Planeten könnt ihr bauen
    :abbr:`z.B. (zum Beispiel)` mit:

    .. code-block:: console

       $ java -Xmx20g -jar target/protomaps-basemap-HEAD-with-deps.jar --nodemap-type=array --osm_path=~/planet-latest.osm.pbf --output=/data/planet.pmtiles --bounds=planet --tmpdir=/var/scratch

    ``-Xmx20g``
        Gebt der Java-Laufzeitumgebung 20 GB Heap-Speicherplatz.
    ``--nodemap-type=array``
        Eine Build-Option, die sich am besten für die Erzeugung von
        Planetenkacheln eignet.
    ``--tmpdir=/var/scratch``
        Stellt sicher, dass mindestens 512 GB Scratch-Speicherplatz vorhanden
        sind.

    .. tip::
       Für eine Berechnung in weniger als drei Stunden empfehlen sich soviele
       CPU-Kerne wie möglich auf einem Intel Core i9, AMD Ryzen 9 :abbr:`o.ä.
       (oder ähnlichem)`, 64 GB RAM und mindestens 1 TB NVMe-SSD-Speicher.

Eigene Tags
    Mit  der Option ``extra_name_tags`` könnt ihr zusätzliche Tags von
    OpenStreetMap in die Ausgabedatei übernehmen.

Tilemaker
---------

`Tilemaker <https://github.com/systemed/tilemaker>`_ ist ein Programm zur
Erstellung von Basiskarten-Kacheln aus OpenStreetMap, allerdings nicht solche,
die mit den `Basemap Layers <https://docs.protomaps.com/basemaps/layers>`__ von
Protomaps übereinstimmen. Darüberhinaus sind die von Tilemaker erzeugten
PMTiles-Archive auch nicht geclustert, was beim Dekodieren in einem Webbrowser
zu großen, langsamen Abrufen führen kann. Für den Produktionseinsatz solltet ihr
daher das Archiv mit `pmtiles cluster
<https://docs.protomaps.com/pmtiles/cli#cluster>`_ optimieren.
