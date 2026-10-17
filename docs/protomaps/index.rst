Protomaps
=========

`Protomaps <https://protomaps.com>`_ ist ein Open-Source-Projekt für die
Erstellung und Nutzung von interaktive Webkarten. Es wurde als leichtgewichtige
Alternative zu herkömmlichen Kartenanbietern entwickelt und bietet eine Reihe
von Vorteilen:

Open Source
    Vollständig offener Quellcode für maximale Transparenz und Anpassbarkeit.
Self-Hosting
    Karten können auf S3 oder eigenen Web-Servern gehostet werden, ohne
    Abhängigkeit von externen Diensten.
Privatsphäre
    Die Karten können sicher und datenschutzfreundlich veröffentlicht werden,
    ohne dass Tracking-Mechanismen wie bei vielen kommerziellen Kartendiensten
    verwendet werden.
Kompaktes Format
    :ref:`python4datascience:pmtiles` ist ein Archivformat aus einer einzigen
    Datei für Pyramiden aus gekachelten Daten. Es kann über `HTTP Range Requests
    <https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Range_requests>`_
    erschlossen werden.
Offline-Nutzung
    Die Karten können vollständig offline verwendet werden, sodass sie
    zuverlässig auch in Krisengebieten verwendt werden können.

Dies ermöglicht kostengünstige und wartungsfreie Kartenanwendungen.

Anwendungsbereiche
------------------

Protomaps eignet sich besonders für:

- Webentwickler, die Karten in ihre Anwendungen integrieren möchten.
- Projekte mit begrenzter Bandbreite oder für Regionen mit eingeschränkter
  Internetverbindung
- datenschutzsensible Anwendungen, die keine Daten an Dritte senden sollen
- Kartenanwendungen, die unabhängig von kommerziellen Anbietern funktionieren
  sollen

Alternativen
------------

PMTiles ist ein schreibgeschütztes Format, sodass es nicht an Ort und Stelle
aktualisiert werden kann, ohne die gesamte Datei neu zu schreiben. Wenn ihr
transaktionale Aktualisierungen benötigt, verwendet eine Datenbank wie
:doc:`SQLite <python-basics:save-data/sqlite/index>` oder
:doc:`python4datascience:data-processing/postgresql/postgis/index` und
`ST_asMVT <https://postgis.net/docs/ST_AsMVT.html>`_.

.. seealso::
   * :ref:`python4datascience:mvt`
   * :ref:`python4datascience:mbtiles`
   * :ref:`python4datascience:cog`

Javascript-Integrationen
------------------------

PMTiles ist für die direkte Anzeige in Webbrowsern in Verbindung mit einer
JavaScript-Bibliothek konzipiert, darunter:

- `Maplibre GL JS <https://maplibre.org/maplibre-gl-js/docs/>`_
- `Leaflet <https://leafletjs.com>`_
- `OpenLayers <https://openlayers.org>`_

Datenquellen
------------

Protomaps stellt auch kartografische :doc:`Basiskarten <basemaps>` bereit, die
:abbr:`u. a. (unter anderem)` auf `OpenStreetMap
<https://www.openstreetmap.org/>`_ basieren und als großes PMTiles-Archivr
bereitgestellt werden. Es können jedoch auch eigene Daten ergänzt werden.

.. toctree::
    :hidden:
    :titlesonly:
    :maxdepth: 0

    extract
    convert
    basemaps
    publish
    cli
