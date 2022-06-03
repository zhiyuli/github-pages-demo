.. Github Pages Demo documentation master file, created by
   sphinx-quickstart on Thu Jun  2 14:49:01 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Creating Github Pages for Code
==============================

|SphinxBuild| |Deploy|

.. |SphinxBuild| image:: https://github.com/cybergis/github-pages-demo/actions/workflows/SphinxBuild.yml/badge.svg
    :target: https://github.com/cybergis/github-pages-demo/actions/workflows/SphinxBuild.yml

.. |Deploy| image:: https://github.com/cybergis/github-pages-demo/actions/workflows/pages/pages-build-deployment/badge.svg
    :target: https://github.com/cybergis/github-pages-demo/actions/workflows/pages/pages-build-deployment

**Author:** `Alexander Michels <https://alexandermichels.github.io/>`_

It's increasingly common for software and projects to have documentation sites with auto-generated docs and/or examples using Jupyter notebooks. Some examples include:

* `geopanda documentation and examples <https://geopandas.org/en/stable/>`_
* `osmnx documentation <https://osmnx.readthedocs.io/en/stable/osmnx.html>`_

Some `CyberGIS Center <https://cybergis.illinois.edu/>`_ projects with sites include:

* `cybergisx-cli <https://cybergis.github.io/cybergisx-cli/>`_ (made with `MkDocs <https://www.mkdocs.org/>`_)
* `cybergis-compute-python-sdk <https://cybergis.github.io/cybergis-compute-python-sdk/>`_ (made with `Sphinx <https://www.sphinx-doc.org/en/master/>`_)

This site has the goal of walking through how to create one of these sites with Sphinx. At the end of the tutorial, you could end up with the `Examples page <examples.html>`_ and `User Reference page <reference.html>`_.

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   tutorial
   examples
   reference



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
