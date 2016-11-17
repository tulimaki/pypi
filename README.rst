Shuup Python Package Index
==========================

This is a PyPI index of Shuup releases.

The index is hosted by Github Pages on https://shuup.github.io/pypi/simple/

Usage
-----

You can use the ``--extra-index-url`` parameter to ``pip`` to access the extra index.

This works both on the command line::

  pip install --extra-index-url https://shuup.github.io/pypi/simple/ shuup==0.5.0
  
and in a ``requirements.txt`` file::

  --extra-index-url https://shuup.github.io/pypi/simple/
  shuup==0.5.0
  # ... other packages ...

How to release a new package
----------------------------

* Create a virtualenv and add the `compoze`_ tool::
  
    virtualenv venv
    . venv/bin/activate
    pip install compoze
 
* Add the new file (e.g. a wheel) to the repository
* Blow the old ``simple`` index away and regenerate it using ``compoze``::

    rm -fr simple
    compoze index

* Add everything to Git and commit::

    git add --all .
    git commit -m "Add Shuup X.Y.Z"

.. _compoze: https://pypi.python.org/pypi/compoze
