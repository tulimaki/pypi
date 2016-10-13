Shuup Python Package Index
==========================

This is a PyPI index of Shuup releases.  To release a new package
(e.g. wheel) put the file here and regenare the simple index with
following commands::

  virtualenv venv
  . venv/bin/activate
  pip install compoze
  rm -fr simple
  compoze index

Then add everything to Git and commit::

  git add .
  git commit -m "Add Shuup X.Y.Z"
