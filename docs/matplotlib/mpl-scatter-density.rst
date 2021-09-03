mpl-scatter-density
===================

`mpl-scatter-density <https://github.com/astrofrog/mpl-scatter-density>`_
erleichtert das Erstellen interkativer Streudichtekarten aus großen Datenmengen.

Installation
------------

.. code-block:: console

    $ pipenv install mpl-scatter-density

Damit werden atuomatisch auch die Abhängigkeiten `Numpy <https://numpy.org/>`_,
:doc:`index` und `fast-histogram <https://github.com/astrofrog/fast-histogram>`_
installiert.

Verwendungszweck
----------------

.. code-block:: python

    import  numpy  as  np 
    import  mpl_scatter_density 
    import  matplotlib . pyplot  als  plt

.. code-block:: python

    # Generate fake data

    N = 10000000
    x = np.random.normal(4, 2, N)
    y = np.random.normal(3, 1, N)

Es gibt im Wesentlichen zwei Verweundungszwecke für mpl-scatter-density,
``projection='scatter_density'`` und ``ScatterDensityArtist``.

``projection='scatter_density'``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: python

    fig = plt.figure()
    ax = fig.add_subplot(1, 1, 1, projection='scatter_density')
    ax.scatter_density(x, y)
    ax.set_xlim(-5, 10)
    ax.set_ylim(-5, 10)
    fig.savefig('gaussian.png')

``ScatterDensityArtist``
~~~~~~~~~~~~~~~~~~~~~~~~

Auch im vorhergehenden Beispiel wird ``ScatterDensityArtist`` verwendet, ohne es
jedoch direkt anzugeben. Im folgenden Beispiel fügen wir es explizit den Achsen
hinzu:

.. code-block:: python

    from mpl_scatter_density import ScatterDensityArtist
    a = ScatterDensityArtist(ax, x, y)
    ax.add_artist(a)
