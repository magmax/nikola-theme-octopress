What is this?
=============

This is the `Octopress classic theme`_, ported to be used with Nikola_.

How to install it?
==================

In your Nikola_ site:

#. Create the ``themes`` directory and enter on it.
#. Clone this repository there, naming it ``octopress``::

     git clone git@github.com:magmax/nikola-theme-octopress.git octopress

#. Edit your ``conf.py``, setting the variable ``THEME`` to ``octopress``::

     THEME = "octopress"

#. Build again::

     $ nikola build

That's it!

.. _`Octopress classic theme`: https://github.com/octopress/classic-theme
.. _`Nikola`: http://getnikola.com/
