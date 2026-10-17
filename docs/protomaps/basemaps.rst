Basemaps
========

Die Protomaps-Basiskarte basiert auf `OpenStreetMap
<https://www.openstreetmap.org/>`_- und `Natural Earth
<https://www.naturalearthdata.com>`_-Daten. Sie enthält nicht alle Daten und
Tags von :abbr:`OSM (OpenStreetMap)`; stattdessen ist sie so konzipiert, dass
sie ein ausgewogenes Verhältnis zwischen Kachelgröße und Vollständigkeit bietet,
um als allgemeine Kontextkarte verwendet werden zu können. Die Organisation der
Ebenen und Tags ist vom Open-Source-Projekt `Tilezen
<https://tilezen.readthedocs.io/en/latest/layers/>`_ abgeleitet. Der Umfang der
Inhalte und die Auswahl der Daten, die bei bestimmten Zoomstufen einbezogen
werden, spiegeln sich in den Referenzimplementierungen von Tilezen-Stilen wie
:abbr:`z. B. (zum Beispiel)` `Bubble Wrap
<https://tangrams.github.io/bubble-wrap/>`_ wider.

.. seealso::
   * `Basemap Layers
     <https://docs.protomaps.com/basemaps/layers#basemap-layers>`_

Das `protomaps/basemaps <https://github.com/protomaps/basemaps>`__-Repository
ist im Wesentlichen in folgende Teile gegliedert:

`/app <https://github.com/protomaps/basemaps/tree/main/app>`_
    enthält eine Single-Page-App unter https://maps.protomaps.com zum Anzeigen
    und Herunterladen von Basiskarten-Builds.
`/tiles <https://github.com/protomaps/basemaps/tree/main/tiles>`_
    enthält ein `Planetiler <https://github.com/onthegomap/planetiler>`_-Profil,
    das :file:`planet.pmtiles` aus OpenStreetMap- und Natural Earth-Daten
    generiert.
`/styles <https://github.com/protomaps/basemaps/tree/main/styles>`_
    enthält ein TypeScript-Paket, das `MapLibre GL JS
    <https://maplibre.org/maplibre-gl-js/docs/>`_-Stile in verschiedenen
    Farbthemen generiert, die über npm verwendet oder als JSON exportiert werden
    können. Ressourcen wie Schriftarten und Sprites werden jedoch im Repository
    `basemaps-assets <https://github.com/protomaps/basemaps-assets>`_ gehostet
    und stehen dort zum Download bereit.

#. Ihr benötigt Java 25 oder höher sowie Maven und nvm:

   .. tab:: Windows

      .. code-block:: ps1

         > choco install openjdk maven
         > curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.8/install.sh | bash
         > nvm install

   .. tab:: MacOS

      .. code-block:: console

         $ brew install temurin maven
         $ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.8/install.sh | bash
         $ nvm install

   .. tab:: Debian/Ubuntu

      .. code-block:: console

         $ apt install openjdk-25-jdk maven
         $ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.8/install.sh | bash
         $ nvm install

#. Klonen des Basemap-Repository:

   .. code-block:: console

      $ git clone https://github.com/protomaps/basemaps.git

#. Wechseln in das :file:`tiles`-Verzeichnis , laden der Abhängigkeiten und
   kompilieren der :file:`*.jar`-Datei:

   .. code-block:: console

      $ cd basemaps/tiles
      $ mvn clean package
      ...
      [INFO] Building jar: /Users/veit/basemaps/tiles/target/protomaps-basemap-HEAD-with-deps.jar
      [INFO] ------------------------------------------------------------------------
      [INFO] BUILD SUCCESS
      [INFO] ------------------------------------------------------------------------
      [INFO] Total time:  49.707 s
      [INFO] Finished at: 2026-10-20T13:06:50+02:00
      [INFO] ------------------------------------------------------------------------

#. Ressourcen für OSM-Wasser- und Landpolygone, `Natural Earth
   <https://www.naturalearthdata.com>`_, Sprachunterstützung und Ranking
   herunterladen und generieren der :file:`berlin.pmtiles`-Datei im aktuellen
   Verzeichnis:

   .. code-block:: console

      $ java -jar target/*-with-deps.jar --download --force --area=berlin
      ...
      0:08:04 DEB [archive] -    Max tile: 232k (gzipped: 138k)
      0:08:04 DEB [archive] -    Avg tile: 64k (gzipped: 44k) using weighted average based on OSM traffic
      0:08:04 DEB [archive] -     # tiles: 4.546
      0:08:04 DEB [archive] -  # features: 4.595.171
      0:08:04 INF [archive] - Finished in 6s cpu:1m4s avg:10
      0:08:04 INF [archive] -   read    1x(9 % 0,6s done:6s)
      0:08:04 INF [archive] -   encode 11x(66 % 4s)
      0:08:04 INF [archive] -   write   1x(1 % 0,1s wait:6s)
      0:08:04 INF [archive] - Finished in 8m4s cpu:6m27s avg:0,8
      0:08:04 INF [archive] - FINISHED!
      ...
      0:08:04 INF [archive] -   archive    61MB
      0:08:04 INF [archive] -   features   311MB

   ``--download``
       lädt Eingangsquellen automatisch herunter.
   ``--force``
       überschreibt die vorhandene Ausgabedatei.
   :samp:`--area={NAME}`
       gibt den Name des herunterzuladenden `Geofabrik-Gebiets
       <https://download.geofabrik.de/>`_ oder den Dateinamen im Verzeichnis
       :file:`/tiles/data/sources/` an.

   Mit ``--help`` erhaltet ihr eine Liste aller möglichen Optionen.

#. Wechseln in das :file:`app/`-Verzeichnis, um das Karten-Frontend aufzurufen:

   .. code-block:: console

      $ cd ../app/
      $ nvm use
      $ npm ci
      $ npm run dev

#. In eurem Web-Browser könnt ihr nun die URL http://localhost:5173/ aufrufen
   und eure generierte :file:`berlin.pmtiles`-Datei hierher ziehen, um sie
   anzuzeigen:

   .. figure:: berlin-basemap.png
      :alt: Basemap von Berlin

Die Vorteile einer selbst erstellten Basiskarte sind unter anderem:

Aktuelle Basiskarten
    Erstellt Kacheln aus bestimmten OpenStreetMap-Schnappschüssen, :abbr:`z. B.
    (zum Beispiel)` aus den aktuellen Daten von `SliceOSM
    <https://slice.openstreetmap.us/>`_ oder aus vorgenerierten Daten von
    `Geofabrik Downloads <https://download.geofabrik.de>`_.

Ausschnitte
    Erstellt benutzerdefinierte, fokussierte Gebietskarten.

Selbstverständlich könnt ihr auch eine benutzerdefinierte Karte des gesamten
Planeten bauen :abbr:`z.B. (zum Beispiel)` mit:

.. code-block:: console

   $ java -Xmx40g -jar target/protomaps-basemap-HEAD-with-deps.jar --nodemap-type=array --osm_path=~/planet-latest.osm.pbf --output=/data/planet.pmtiles --bounds=planet --tmpdir=/var/scratch

``-Xmx40g``
    gibt der Java-Laufzeitumgebung 40 GB Heap-Speicherplatz.
``--nodemap-type``
    erlaubt euch die Auswahl der geeigneten Build-Option für die Erstellung der
    Planetendatei.
``--tmpdir``
    erlaubt euch die Angabe des Pfades zu einem tempärären Verzeichnis, wofür
    jedoch mindestens 512 GB Scratch-Speicherplatz vorhanden sein sollten.

.. tip::
   Für eine Berechnung in weniger als drei Stunden empfehlen sich soviele
   CPU-Kerne wie möglich auf einem Intel Core i9, AMD Ryzen 9 :abbr:`o. ä.
   (oder ähnlichem)`, 64 GB RAM und mindestens 1 TB SSD-Speicher.

Tilemaker
---------

`Tilemaker <https://github.com/systemed/tilemaker>`_ ist ein alternatives
Programm zur Erstellung von Basiskarten-Kacheln aus OpenStreetMap, allerdings
nicht solche, die mit den `Basemap Layers
<https://docs.protomaps.com/basemaps/layers>`__ von Protomaps übereinstimmen.
Darüberhinaus sind die von Tilemaker erzeugten PMTiles-Archive auch nicht
geclustert, was beim Dekodieren in einem Webbrowser zu großen, langsamen Abrufen
führen kann. Für den Produktionseinsatz solltet ihr daher das Archiv mit
`pmtiles cluster <https://docs.protomaps.com/pmtiles/cli#cluster>`_ optimieren.
