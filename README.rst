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


Configuration
=============

This theme has some improvements over tipical Nikola_ themes, and they can be configured from the ``conf.py`` file.

To configure them, you can use the ``GLOBAL_CONTEXT`` variable. I will show an example later.

Options
-------

asides
~~~~~~

Sorted list of sections to be shown in the sidebar. You can choose these blocks:

google_ads
__________

Will show Google adsense ads. You need to configure the ``google_ads`` variable as well.

github
______

Shows the latest updated GitHub repositories. You need to configure the ``github`` variable as well.

disqus_last_comments
____________________

Shows a list of the latest comments in disqus. You need to configure the ``disqus`` variable as well.

google_plus
___________

Shows the ``+1`` banner. No additional configuration is required.



google_ads
~~~~~~~~~~

Dictionary with keys:

pub
___

Public advertisement id, taken from Google Adsense.

slot
____

Slot given by Google Adsense as well.

width
_____

Advertisement width

height
______

Advertisement height


github
~~~~~~

username
________

Github username

items
_____

Number of repositories to show. Default is 3.


disqus
~~~~~~

username
________

Disqus username

last_items
__________

Number of items to be shown.


Example
-------

It seems difficult, but with this example you are going to understand it easily:

    google_ads = {
      'pub': '1887364423515042',
      'slot': '7479875641',
      'width': 180,
      'height': 150,
    }

    github = {
      'username': 'magmax'
      'items': 3
    }

    disqus = {
      'username': 'magmax'
      'last_items': 5
    }

    GLOBAL_CONTEXT = {
      'asides': ['google_ads', 'github', 'google_plus', 'disqus_last_comments'],
      'google_ads': google_ads,
      'github': github,
      'disqus': disqus,
    }



.. _`Octopress classic theme`: https://github.com/octopress/classic-theme
.. _`Nikola`: http://getnikola.com/
