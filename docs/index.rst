Daten visualisieren
===================

Das Tutorial gibt einen Überblick über die verschiedenen Python-Bibliotheken,
die ihr zur Datenvisualisierung einsetzen könnt. Es ist entstanden aus den
cusy-Schulungen zur `Datenvisualisierung mit Python
<https://cusy.io/de/unsere-schulungsangebote/python-schulungen-fuer-analysten-wissenschaftler-und-ingenieure>`_.

Aktuell ist es sehr schwierig, einen :doc:`overview` zu erhalten. Im Folgenden
versuchen wir, die Suche nach der passenden Bibliothek zu vereinfachen, indem
wir einige Aspekte genauer beleuchten:

* :ref:`technologies`
* :ref:`core-libs`
* :ref:`pandas-plot-api`
* :ref:`further-high-level-apis`
* :ref:`big-data`
* :ref:`chart-types` (Statistische Darstellungen, regelmäßige und
  unregelmäßige Gitter :abbr:`etc. (et cetera)`)

Anschließend geben wir eine praktische Einführung in die gebräuchlichsten
Python-Bibliotheken.

Wir behandeln hier jedoch nicht :doc:`Design-Prinzipien
<cusy-design:viz/diagram-anatomy/index>`, den
:doc:`cusy-design:viz/diagram-anatomy/index`, :doc:`Data-Storytelling
<cusy-design:viz/data-storytelling>` oder die :doc:`Auswahl des passenden
Diagrammtyps <cusy-design:viz/types/index>`. Hierzu verweisen wir jedoch gerne
auf das :doc:`cusy-design:index`.

Darüberhinaus ist das PyViz-Tutorial Teil einer Reihe von Tutorials zur
Datenanalyse und -visualisierung:

* `Python Basics <https://python-basics-tutorial.readthedocs.io/de/latest/>`_
* :doc:`jupyter-tutorial:index`
* :doc:`python4datascience:index`

Alle Tutorials dienen als Seminarunterlagen für unsere aufeinander abgestimmten
Trainings:

+---------------+--------------------------------------------------------------+
| Dauer         | Titel                                                        |
+===============+==============================================================+
| 3 Tage        | `Einführung in Python`_                                      |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Fortgeschrittenes Python`_                                  |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Entwurfsmuster in Python`_                                  |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Effizient Testen mit Python`_                               |
+---------------+--------------------------------------------------------------+
| 1 Tag         | `Software-Dokumentation mit Sphinx`_                         |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Technisches Schreiben`_                                     |
+---------------+--------------------------------------------------------------+
| 3 Tage        | `Jupyter-Notebooks für effiziente Data-Science-Workflows`_   |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Numerische Berechnungen mit NumPy`_                         |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Daten analysieren mit pandas`_                              |
+---------------+--------------------------------------------------------------+
| 3 Tage        | `Daten lesen, schreiben und bereitstellen mit Python`_       |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Daten bereinigen und validieren mit Python`_                |
+---------------+--------------------------------------------------------------+
| 5 Tage        | `Daten visualisieren mit Python`_                            |
+---------------+--------------------------------------------------------------+
| 1 Tag         | `Datenvisualisierungen gestalten`_                           |
+---------------+--------------------------------------------------------------+
| 2 Tage        | `Dashboards erstellen`_                                      |
+---------------+--------------------------------------------------------------+
| 3 Tage        | `Code und Daten versioniert und reproduzierbar speichern`_   |
+---------------+--------------------------------------------------------------+
| Abonnement    | `Neues aus Python für Data-Science`_                         |
| à 2 h im      |                                                              |
| Quartal       |                                                              |
+---------------+--------------------------------------------------------------+

.. _`Einführung in Python`:
   https://cusy.io/de/unsere-schulungsangebote/einfuehrung-in-python
.. _`Fortgeschrittenes Python`:
   https://cusy.io/de/unsere-schulungsangebote/fortgeschrittenes-python
.. _`Entwurfsmuster in Python`:
   https://cusy.io/de/unsere-schulungsangebote/entwurfsmuster-in-python
.. _`Effizient Testen mit Python`:
   https://cusy.io/de/unsere-schulungsangebote/effizient-testen-mit-python
.. _`Software-Dokumentation mit Sphinx`:
   https://cusy.io/de/unsere-schulungsangebote/software-dokumentation-mit-sphinx
.. _`Technisches Schreiben`:
   https://cusy.io/de/unsere-schulungsangebote/technisches-schreiben
.. _`Jupyter-Notebooks für effiziente Data-Science-Workflows`:
   https://cusy.io/de/unsere-schulungsangebote/jupyter-notebooks-fuer-effiziente-data-science-workflows
.. _`Numerische Berechnungen mit NumPy`:
   https://cusy.io/de/unsere-schulungsangebote/numerische-berechnungen-mit-numpy
.. _`Daten analysieren mit pandas`:
   https://cusy.io/de/unsere-schulungsangebote/daten-analysieren-mit-pandas
.. _`Daten lesen, schreiben und bereitstellen mit Python`:
   https://cusy.io/de/unsere-schulungsangebote/daten-lesen-schreiben-und-bereitstellen-mit-python
.. _`Daten bereinigen und validieren mit Python`:
   https://cusy.io/de/unsere-schulungsangebote/daten-bereinigen-und-validieren-mit-python
.. _`Daten visualisieren mit Python`:
   https://cusy.io/de/unsere-schulungsangebote/daten-visualisieren-mit-python
.. _`Datenvisualisierungen gestalten`:
   https://cusy.io/de/unsere-schulungsangebote/datenvisualisierungen-gestalten
.. _`Dashboards erstellen`:
   https://cusy.io/de/unsere-schulungsangebote/dashboards-erstellen
.. _`Code und Daten versioniert und reproduzierbar speichern`:
   https://cusy.io/de/unsere-schulungsangebote/code-und-daten-versioniert-und-reproduzierbar-speichern
.. _`Neues aus Python für Data-Science`:
   https://cusy.io/de/unsere-schulungsangebote/neues-aus-python-fuer-data-science

.. toctree::
    :titlesonly:
    :maxdepth: 0
    :hidden:

    first-steps
    overview
    matplotlib/index
    vega/index
    bokeh/index
    opengl/index
    d3js/index
    js/index
