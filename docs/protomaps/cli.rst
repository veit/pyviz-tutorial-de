pmtiles-CLI-Referenz
====================

``pmtiles show``
----------------

:samp:`$ pmtiles show {FILE}.pmtiles`
    gibt die Header-Informationen und Metadaten eines lokalen Archivs aus.
:samp:`$ pmtiles show https://maps.cusy.io/map.pmtiles`
    gibt die Header-Informationen und Metadaten eines entfernten HTTPS-Archivs
    aus.
:samp:`$ pmtiles show {FILE}.pmtiles --bucket=s3://{BUCKET}`
    gibt die Header-Informationen und Metadaten eines Archivs aus, das sich auf
    einem S3-kompatiblen Bucket befindet.
:samp:`$ pmtiles show {FILE}.pmtiles --header-json`
    gibt eine JSON-Repräsentation des Headers aus.
:samp:`$ pmtiles show {FILE}.pmtiles --metadata`
    gibt die JSON-Metadaten aus.

.. note::
   URLs mit Zeichen wie ``?`` und ``&``, sollten mit einem Backslash ``\``
   escaped werden.

``pmtiles tile``
----------------

:samp:`$ pmtiles tile {FILE}.pmtiles 0 0 0`
    gibt den Inhalt einer einzelnen Kachel aus.

``pmtiles verify``
------------------

:samp:`$ pmtiles verify {FILE}.pmtiles`
    überprüft, ob ein Archiv richtig geordnet ist und korrekte
    Header-Informationen enthält.

``pmtiles extract``
-------------------

:samp:`$ pmtiles extract`
    erstellt ein kleineres Archiv aus einem größeren, wobei da Quellarchiv
    geclustert sein muss:

    :samp:`$ pmtiles extract {IN}.pmtiles {OUT}.pmtiles --bbox=MIN_LON,MIN_LAT,MAX_LON,MAX_LAT`
        Den Begrenzungsrahmen mit ``MIN_LON``, ``MIN_LAT``, ``AX_LON`` und
        ``MAX_LAT`` könnt ihr :abbr:`z.B. (zum Beispiel)` mit `bboxfinder.com
        <https://bboxfinder.com/>`_ ermitteln.

    :samp:`$ pmtiles extract {IN}.pmtiles {OUT}.pmtiles --region={REGION}.geojson`
        Mit ``--region`` kann ein GeoJSON ``Polygon``-, ``Multipolygon``-,
        ``Feature``- oder ein ``FeatureCollection``-Objekt angegeben werden.

    :samp:`$ pmtiles extract https://{EXAMPLE.COM}/{IN}.pmtiles {OUT}.pmtiles --maxzoom={MAXZOOM} --download-threads=4`
        ``--maxzoom`` extrahiert nur eine Teilmenge der Zoomstufen.

        ``--download-threads`` gibt die  Anzahl der parallelen Anfragen zur
        Beschleunigung der Downloads an.

    :samp:`$ pmtiles extract {IN}.pmtiles {OUT}.pmtiles --maxzoom=MAXZOOM --bucket=s3://{BUCKET}`

    Weitere Optionen sind:

    ``--minzoom``
        extrahiert nur einen Teil der Pyramide, was jedoch viel mehr Anfragen
        erfordern kann als die Standardeinstellung ``--minzoom=0``. Da dies die
        Übersichts-Zoomstufen entfernt, sollte es nur in bestimmten Situationen
        verwendet werden.
    ``--overfetch``
        läd zusätzliche Daten herunter, um kleine Anfragen zu bündeln: ``0.05``
        entspricht 5 %.

``pmtiles serve``
-----------------

:samp:`$ pmtiles serve`
    ist ein einfacher Weg, PMTiles zusammen mit `pmtiles.js
    <https://www.npmjs.com/package/pmtiles>`_ im Web bereitzustellen:

    :samp:`$ pmtiles serve {PATH}`
        liefert eine :samp:`{TILESET}.pmtiles`-Datei aus dem Verzeichnis
        :samp:`{PATH}` unter der URL
        :samp:`http://localhost:8080/{TILESET}/{Z}/{X}/{Y}.mvt|png|jpg|webp|avif`
        aus, wobei der Suffix dem Kacheltyp im Archiv entsprechen muss.

    :samp:`$ pmtiles serve . --public-url=localhost`
        erlaubt die Ausgabe von `TileJSON
        <https://github.com/mapbox/tilejson-spec/tree/master/3.0.0>`_ unter der
        URL :samp:`http://localhost:8080/{TILESET}.json`.

``pmtiles convert``
-------------------

:samp:`$ pmtiles convert`
    konvertiert ein `MBTiles
    <https://docs.mapbox.com/help/glossary/mbtiles/>`_-Archiv in PMTiles:

    :samp:`$ pmtiles convert {IN}.mbtiles {OUT}.pmtiles`

    :samp:`--no-deduplication`
        Kachelinhalte sollten üblicherweise de-dupliziert werden. Verwendet dies
        nur, wenn ihr wisst, dass die Eingabe nur einzigartige Kacheln enthält
        und die Konvertierung beschleunigt werden soll.
    :samp:`--tmpdir`
        erlaubt die Angabe des temporären Verzeichnisses.

``pmtiles cluster``
-------------------

:samp:`pmtiles cluster {IN}.pmtiles`
    clustert ein bestehendes Archiv, wobei die Größe und das Layout optimiert
    werden. Mit `tippecanoe <https://github.com/felt/tippecanoe>`_,
    `planetiler <https://github.com/onthegomap/planetiler>`_ und pmtiles CLI
    erstellte Archive sind bereits geclustert.

    :samp:`--no-deduplication`
        Kachelinhalte sollten üblicherweise de-dupliziert werden. Verwendet dies
        nur, wenn ihr wisst, dass die Eingabe nur einzigartige Kacheln enthält
        und die Konvertierung beschleunigt werden soll.

``pmtiles upload``
------------------

:samp:`pmtiles upload {IN}.pmtiles {REMOTE}.pmtiles --bucket=s3://{BUCKET}`
    lädt ein Archiv in den Cloud-Speicher hoch.

``pmtiles edit``
----------------

:samp:`pmtiles edit NAME.pmtiles --header-json={HEADER}.json --metadata={METADATA}.json`
    ändert Teile des Archiv-Headers, oder ersetzt die JSON-Metadaten des
    Archivs. Wenn ihr nur den Header bearbeitet, wird die Datei an Ort und
    Stelle geändert; das Schreiben der JSON-Metadaten erfordert jedoch das
    Schreiben einer neuen Kopie des Archivs, die dann :samp:`NAME.pmtiles`
    ersetzt.

    .. hint::
       Ihr könnt die bestehenden Header-Informationen und Metadaten in die
       Dateien :samp:`{HEADER}.json` und :samp:`{METADATA}.json` schreiben mit:

       :samp:`pmtiles show {NAME}.pmtiles --header-json > {HEADER}.json`

       :abbr:`bzw. (beziehungsweise)`

       :samp:`pmtiles show {NAME}.pmtiles --metadata > {METADATA}.json`

    .. hint::
       Die Felder ``tile_type``, ``tile_compresssion``, ``minzoom``,
       ``maxzoom``, ``bounds`` und ``center`` des Headers können bearbeitet
       werden; andere Felder sind jedoch nicht bearbeitbar.

``pmtiles version``
-------------------

:samp:`pmtiles version`
    gibt die Version von pmtiles aus.
