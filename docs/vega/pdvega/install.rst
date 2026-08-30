PdVega-Installation
===================

PdVega kann installiert werden mit

.. code-block:: console

    $ uv add pdvega
    $ uv run jupyter nbextension install --sys-prefix --py vega3
    …
    - Validating: OK

        To initialize this nbextension in the browser every time the notebook (or other app) loads:

              jupyter nbextension enable vega3 --py --sys-prefix

.. seealso::
   * `Installing and Using pdvega
     <https://altair-viz.github.io/pdvega/installation.html#installation>`_

Abhängigkeiten
--------------

Um Plots als PNG oder SVG speichern zu können, müssen die
Kommandozeilenwerkzeuge ``vl2png`` und ``vl2svg`` aus dem `vega-lite
<https://github.com/vega/vega-lite>`_-npm-Paket vorhanden sein.
