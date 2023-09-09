Schnelleinstieg
===============

.. image:: https://img.shields.io/github/contributors/veit/pyviz-tutorial.svg
   :alt: Contributors
   :target: https://github.com/veit/pyviz-tutorial/graphs/contributors
.. image:: https://img.shields.io/github/license/veit/pyviz-tutorial.svg
   :alt: License
   :target: https://github.com/veit/pyviz-tutorial/blob/main/LICENSE
.. image:: https://results.pre-commit.ci/badge/github/veit/pyviz-tutorial/main.svg
   :alt: pre-commit.ci status
   :target: https://results.pre-commit.ci/latest/github/veit/pyviz-tutorial/main
.. image:: https://readthedocs.org/projects/pyviz-tutorial/badge/?version=latest
   :alt: Docs
   :target: https://pyviz-tutorial.readthedocs.io/de/latest/
.. image:: https://pyup.io/repos/github/veit/pyviz-tutorial/shield.svg
   :alt: Pyup
   :target: https://pyup.io/repos/github/veit/pyviz-tutorial/
.. image:: https://img.shields.io/badge/dynamic/json?label=Mastodon&query=totalItems&url=https%3A%2F%2Fmastodon.social%2F@PyViz%2Ffollowers.json&logo=mastodon
   :alt: Mastodon
   :target: https://mastodon.social/@PyViz

Installation
------------

#. Herunterladen und Auspacken:

   .. code-block:: console

    $ curl -O https://codeload.github.com/veit/pyviz-tutorial/zip/refs/heads/main
    $ unzip main
    Archive:  main
    …
       creating: pyviz-tutorial-main/
    …

#. Pandoc installieren:

   * für Ubuntu und Debian:

     .. code-block:: console

        $ sudo apt install pandoc

   * für Mac OSX:

     .. code-block:: console

        $ brew install pandoc

#. Python-Pakete installieren:

   .. code-block:: console

    $ cd pyviz-tutorial
    $ python3 -m venv .
    $ bin/python -m pip install  --upgrade pip setuptools
    $ bin/python -m pip install -r requirements.txt

#. HTML-Dokumentation erstellen:

   .. code-block:: console

    $ bin/sphinx-build -b html docs/ docs/_build/

#. PDF erstellen:

   Für die Erstellung von PDFs benötigt ihr weitere Pakete.

   Für Debian/Ubuntu erhaltet ihr diese mit:

   .. code-block:: console

    $ apt-get install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended latexmk

   oder für Mac OS X mit:

   .. code-block:: console

    $ brew cask install mactex
    …
    🍺  mactex was successfully installed!
    $ curl --remote-name https://www.tug.org/fonts/getnonfreefonts/install-getnonfreefonts
    $ sudo texlua install-getnonfreefonts
    …
    mktexlsr: Updating /usr/local/texlive/2020/texmf-dist/ls-R...
    mktexlsr: Done.

   Anschließend könnt ihr ein PDF generieren mit:

   .. code-block:: console

    $ cd docs/
    $ make latexpdf
    …
    The LaTeX files are in _build/latex.
    Run 'make' in that directory to run these through (pdf)latex
    …

   Das PDF findet ihr anschließend in ``docs/_build/latex/pyviz-tutorial.pdf``.

Folge uns
---------

* `GitHub <https://github.com/veit/pyviz-tutorial>`_
* `Twitter <https://twitter.com/PyvizTutorial>`_
* `Mastodon <https://mastodon.social/@PyViz>`_

Pull-Requests
-------------

Wenn ihr Vorschläge für Verbesserungen und Ergänzungen habt, empfehle ich euch,
einen `Fork <https://github.com/veit/pyviz-tutorial/fork>`_ meines
`GitHub-Repository <https://github.com/veit/pyviz-tutorial/>`_ zu erstellen
und darin eure Änderungen vorzunehmen. Gerne dürft ihr auch einen *Pull Request*
stellen. Sofern die darin enthaltenen Änderungen klein und atomar sind, schaue
ich mir eure Vorschläge gerne an.
