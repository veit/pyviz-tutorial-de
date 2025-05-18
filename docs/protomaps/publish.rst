Veröffentlichen
===============

HTTPS
    Ihr könnt euren Kartendienst einfach über HTTPS veröffentlichen.

    HTTPS ist auch für `HTTP/2
    <https://developer.mozilla.org/en-US/docs/Glossary/HTTP_2>`_ erforderlich,
    wodurch die Kartenanzeige auch schneller wird, da dann mehr Anfragen auf
    einmal möglich sind.

CORS
    `Cross-Origin Resource Sharing
    <https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP>`_ schränkt die
    Websites ein, die eure gehosteten Ressourcen einbetten dürfen.

    .. warning::
       Vermeidet Wildcards ``*`` für ``Access-Control-Allow-Origin`` im
       produktiven Einsatz.

Karten-Ressourcen
    Auch wenn eure PMTiles-Archive oder Kachelendpunkte aus eurer eigenen
    Infrastruktur stammen, können andere Ressourcen auf einer Webkarte von
    externen Anbietern stammen. Dazu gehören JavaScript-Bibliotheken,
    CSS-Stylesheets und Schriften.

Content Security Policy
    Durch die Festlegung einer Content Security Policy über einen HTTP-Header
    oder ein HTML-Meta-Tag könnt ihr sicherstellen, dass alle Ressourcen der
    HTML-Seite aus derselben Quelle stammen, :abbr:`z.B. (zum Beispiel)` für
    MapLibre:

    .. code-block:: html

       <meta
         http-equiv="Content-Security-Policy"
         content="default-src 'self' 'nonce-n0nce' 'nonce-n0nce1'; worker-src blob: ; child-src blob: ; img-src data: blob: ;" />

Beispiel
--------

Nachfolgend findet ihr ein vollständiges Beispiel für eine Kartenanwendung, bei
der Quellen von Dritten vermieden werden:

.. literalinclude:: berlin.html
   :language: html
   :linenos:
   :emphasize-lines: 7-10, 18, 26-27, 32

Zeilen 7–10
    :file:`maplibre-gl.js` und :file:`maplibre-gl.css` sind JavaScript und CSS
    für die `MapLibre GL
    <https://maplibre.org/maplibre-gl-js/docs/>`_-Rendering-Bibliothek.

    :file:`pmtiles.js` ist eine JavaScript-Datei zum Dekodieren von
    PMTiles-Archiven im Browser.

    :file:`basemaps.js` ist eine JavaScript-Datei zum Erstellen eines MapLibre
    GL-Stils für ein Basiskarten-Kachelset.

Zeile 18
    :file:`mapbox-gl-rtl-text.min. js` ist ein MapLibre-Plugin für die
    Unterstützung von Sprachen, die von rechts nach links geschrieben werden.

Zeilen 26–27
    :file:`fonts/{fontstack}/{range}.pbf` sind Schriftglyphen für die
    Darstellung von Labels, verfügbar unter `protomaps/basemaps-assets
    <https://github.com/protomaps/basemaps-assets>`_.

    :file:`sprites/{version/{flavor_name}` sind `Sprites
    <https://de.wikipedia.org/wiki/Sprite_(Computergrafik)>`_ für Basemap-Icons,
    verfügbar unter `protomaps/basemaps-assets
    <https://github.com/protomaps/basemaps-assets>`__.
Zeile 32
   :file:`pmtiles://berlin.pmtiles` ist die Archivdatei mit den Kartendaten.

Cloud-Speicher
--------------

PMTiles funktioniert auf jeder S3-kompatiblen Cloud-Speicherplattform, die `HTTP
Range Requests <https://developer.mozilla.org/en-US/docs/Web/HTTP/Range_requests>`_
und `Cross-Origin Resource Sharing (CORS)
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS>`_ unterstützt.

Upload
~~~~~~

Das Kommandozeilentool `pmtiles <https://github.com/protomaps/go-pmtiles>`_
verfügt über den Befehl ``pmtiles upload``, um Dateien in einen Cloud-Speicher
zu übertragen. `RClone <https://rclone.org>`_ ist ein weiteres Tool für die
Verwaltung großer Dateien auf S3-kompatiblem Speicher:

:samp:`rclone copyto {FILENAME} {CONFIGURATION}:{BUCKET}/{FOLDER}/{FILENAME}.pmtiles --progress --s3-chunk-size=256M`

.. seealso::
   * `Recommended Platforms
     <https://docs.protomaps.com/pmtiles/cloud-storage#recommended-platforms>`_

Web-Server
----------

.. _caddy:

Caddy
~~~~~

`Caddy <https://caddyserver.com/>`_ ist wegen seiner eingebauten
HTTPS-Unterstützung sehr empfehlenswert für die Bereitstellung von PMTiles.
Verwendet die ``file_server``-Konfiguration, um :file:`*.pmtiles` aus einem
statischen Verzeichnis mit folgender CORS-Konfiguration bereitzustellen:

.. code-block:: javascript

   header {
     Access-Control-Allow-Methods GET,HEAD
     Access-Control-Expose-Headers ETag
     Access-Control-Allow-Headers Range,If-Match
     Access-Control-Allow-Origin https://www.cusy.io
   }

Als Alternative könnt ihr das `pmtiles_proxy
<https://caddyserver.com/docs/modules/http.handlers.pmtiles_proxy>`_-Plugin
für Caddy verwenden.

.. seealso::
   * `Protomaps Docs: Set up a Server: Caddy
     <https://docs.protomaps.com/deploy/server#caddy>`_

.. _nginx:

nginx
~~~~~

`nginx <https://nginx.org>`_ unterstützt HTTP Range Requests, wobei die
CORS-Header und die Unterstützung für CORS Preflight-Anfragen in der
Konfigurationsdatei gesetzt werden sollten:

.. code-block:: javascript

   if ($request_method = 'OPTIONS') {
     add_header 'Access-Control-Max-Age' 3600;
     add_header 'Content-Type' 'text/plain charset=UTF-8';
     add_header 'Access-Control-Allow-Origin' '*' always;
     add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range' always;
     add_header 'Content-Length' 0;
     return 204;
   }
