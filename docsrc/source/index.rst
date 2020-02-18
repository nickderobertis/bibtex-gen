.. bibtex-gen documentation master file, created by
   cookiecutter-pypi-sphinx.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to BibTeX Generator documentation!
********************************************************************

Generate BibTeX reference objects from DOIs and strings

To get started, look here.

.. toctree::
   :caption: Tutorial

   tutorial
   auto_examples/index

An overview
===========

Quick Links
------------

Find the source code `on Github <https://github.com/nickderobertis/bibtex-gen>`_.


bibtex_gen
-------------------------------------------------------


This is a simple example:

.. code:: python

      import bibtex_gen
      # Note: these are fake credentials. You need to sign up for a Mendeley account, go to Mendeley Developers,
      # and create an "app" which will give you this info.
      mendeley_client_id = '9871'
      mendeley_client_secret = 'sdfa4dfDSSDFasda'
      btg = bibtex_gen.BibTexGenerator(mendeley_client_id, mendeley_client_secret)
      # This object contains all the article data and can be used directly with pyexlatex
      bibtex_obj = btg.generate('10.1111/j.1540-6261.2011.01679.x', 'da-engelberg-gao-2011')
      # Or, multiple at once with a dict
      item_doi_dict = {
          'da-engelberg-gao-2011': '10.1111/j.1540-6261.2011.01679.x',
          'barber-odean-2008': '10.1093/rfs/hhm079',
      }
      # These objects contain all the article data and can be used directly with pyexlatex
      bibtex_objs = btg.generate_from_dict(item_doi_dict)



.. toctree:: api/modules
   :caption: API Documentation
   :maxdepth: 3

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
