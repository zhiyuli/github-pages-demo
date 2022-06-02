Autodocs
========

We will be using the `Napoleon <https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html>`_ extension for Google strings.


#. **Docstrings**

   Let's create and document a single function in ``mycybergis/uiuc.py``.

   An example of Google docstrings::

        Creates and returns a folium.Map instance of UIUC.

        Args:
            center (List[int]): the lon, lat for the center of the map.
            zoom (int): the starting level of zoom.

        Returns:
            folium.Map showing UIUC

#. **Creating Autodocs with Autodoc and Napoleon**

   Now that we have our docstrings, we need to figure out how to generate documentation from it. Create a new page ("reference.rst") in the ``docs/`` and copy/paste the following into it::

        User Reference
        ==============

        User reference for mycybergis package.

        mycybergis.uiuc module
        ----------------------

        .. automodule:: mycybergis.uiuc
            :members:
    
   Let's break this down:

   * The heading of the page is "User Reference"
   * A short textual description
   * A subheading for the module within our package
   * The `autodoc directive <https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#directives>`_ tells us to document the module ``mycybergis.uiuc`` and all of it's members (``:members:``).

#. **Add reference.rst to your TOC tree**

   Your toc tree on index.rst should include reference.rst::

        .. toctree::
            :maxdepth: 2
            :caption: Contents:

            tutorial
            reference

#. **Make HTML**

   Run ``make html`` in ``docs/`` and check the result! See if you can debug any formatting issues that come up!