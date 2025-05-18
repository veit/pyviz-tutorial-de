Protomaps
=========

`Protomaps <https://protomaps.com>`_ ist ein Open-Source-Projekt für die
Erstellung und Nutzung von Vektorkarten. Es wurde als leichtgewichtige
Alternative zu herkömmlichen Kartenanbietern entwickelt und bietet eine Reihe
von Vorteilen.

Open Source
    Vollständig offener Quellcode für maximale Transparenz und Anpassbarkeit.
Selbsthosting
    Karten können auf eigenen Servern gehostet werden, ohne Abhängigkeit von
    externen Diensten.
Privatsphäre
    Die Karten können sicher und datenschutzfreundlich veröffentlicht werden,
    ohne dass Tracking-Mechanismen wie bei vielen kommerziellen Kartendiensten
    verwendet werden.
Kompaktes Format
    Die Kartendaten werden im effizienten `PMTiles
    <https://docs.protomaps.com/pmtiles/>`_-Format gespeichert.
Offline-Nutzung
    Die Karten können vollständig offline verwendet werden, sodass sie
    zuverlässig auch in Krisengebieten verwendt werden können.

Anwendungsbereiche
------------------

Protomaps eignet sich besonders für:

- Webentwickler, die Karten in ihre Anwendungen integrieren möchten.
- Projekte mit begrenzter Bandbreite oder in Regionen mit eingeschränkter
  Internetverbindung
- datenschutzsensible Anwendungen, die keine Daten an Dritte senden sollen
- Kartenanwendungen, die unabhängig von kommerziellen Anbietern funktionieren
  sollen

Technologiestack
----------------

Protomaps kann mit verschiedenen JavaScript-Bibliotheken verwendet werden:

- `Maplibre GL JS <https://maplibre.org/maplibre-gl-js/docs/>`_
- `Leaflet <https://leafletjs.com>`_
- `OpenLayers <https://openlayers.org>`_

Datenquellen
------------

Die Kartendaten stammen hauptsächlich aus `OpenStreetMap
<https://www.openstreetmap.org/>`_, können aber um eigene Daten ergänzt werden.

.. toctree::
    :hidden:
    :titlesonly:
    :maxdepth: 0

    extract
    convert
    publish
    cli
