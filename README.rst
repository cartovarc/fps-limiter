.. image:: https://img.shields.io/pypi/v/fps-limiter.svg
        :target: https://pypi.python.org/pypi/fps-limiter

.. image:: https://pepy.tech/badge/fps-limiter/month
        :target: https://pepy.tech/project/fps-limiter

fps-limiter
===========

Limit while loop at certain fps rate

Installation
------------

.. code:: bash

    pip install fps-limiter

Examples
--------

Example #1
~~~~~~~~~~

.. code:: python


    from fps_limiter import LimitFPS, FPSCounter

    fps_limiter = LimitFPS(fps=15)
    fps_counter = FPSCounter()

    while True:
        if fps_limiter():
            print("current fps: %s" % fps_counter())

Example #2
~~~~~~~~~~

.. code:: python


    from fps_limiter import LimitFPS, FPSCounter

    fps_limiter = LimitFPS(fps=15)

    while True:
        if fps_limiter():
            print("elapsed seconds: %s" % fps_limiter.get_elapsed_seconds())

License
-------

`MIT <https://choosealicense.com/licenses/mit/>`__
