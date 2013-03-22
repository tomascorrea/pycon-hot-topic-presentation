:title: Pycon
:author: Jayson, Chacon e Tomas
:description: Apresentção dos principais pontos observados na pycon.
:keywords: pycon
:css: pycon.css


Pycon 2013 - Santa Claro - California
=====================================

Principais pontos

----

Keynote do Guido
================

API de chamadas asyncronas em python
------------------------------------

.. code:: python

    import requests

    @task
    def my_task(url):
        yield from requests.get(url)


----


raspberry pi
============

Cada participante ganhou um raspberry pi e foram dada varios workshop. Mudar o mundo atraves da educação. Levar tecnologia aos menos favorecidos.

----

The Naming of Ducks
===================

Where Dynamic Types Meet Smart Conventions
------------------------------------------

Em linguages com tipagem estatica o tipo da variavel da uma ideia do que uma variavel, paramentro ou retorno de uma representa. Em linguagens com tipagem dinamica precisamos dar bons
nomes as variaveis classes e funções. O codigo abaixo demonstra quão dificil pode ser entender um código com nomes pouco representativos.


----

The Naming of Ducks
===================

Where Dynamic Types Meet Smart Conventions
------------------------------------------

.. code:: python

    def _11(_12):
        return _r_.get(_12)


----

The Naming of Ducks
===================

Where Dynamic Types Meet Smart Conventions
------------------------------------------

.. code:: python

    def get_page(url):
        return requests.get(url)

----


The drawback with reStructuredText is that you can't skip levels. You can't
go directly from level 1 to level 3 without having a level 2 in between.
If you do you get an error::

    Title level inconsistent

----

Other formatting
================

All the normal reStructuredText functions are supported in Hovercraft!

- Such as bulletlists, which start with a dash (-) or an asterisk (*).
  You can have many lines of text in one bullet if you indent the
  following lines.

   - And you can have many levels of bullets.

       - Like this.

- There is *Emphasis* and **strong emphasis**, rendered as <em> and <strong>.

----

More formatting
===============

#. Numbered lists is of course also supported.

#. They are automatically numbered.

#. But only for single-level lists and single rows of text.

#. ``inline literals``, rendered as <tt> and usually shown with a monospace font, which is good for source code.

#. Hyperlinks, like Python_

.. _Python: http://www.python.org


----

Slides can have presenter notes!
================================

This is the killer-feature of Hovercraft! as very few other tools like this
support a presenter console. You add presenter notes in the slide like this:

.. note::

    And then you indent the text afterwards. You can have a lot of formatting
    in the presenter notes, like *emphasis* and **strong** emphasis.

    - Even bullet lists!

    - Which can be handy!

    But you can't have any headings.


----

Source code
===========

You can also have text that is mono spaced, for source code and similar.
There are several syntaxes for that. For code that is a part of a sentence
you use the inline syntax with ``double backticks`` we saw earlier.

If you want a whole block of preformatted text you can use double colons::

    And then you
    need to indent the block
    of text that
    should be preformatted

You can even have the double colons on a line by themselves:

::

    And this text will
    now be
    rendered as
    preformatted text

----

Syntax highlighting
===================

But the more interesting syntax for preformatted text is the .. code::
directive. This enables you to syntax highlight the code.

.. code:: python

    def day_of_year(month, day):
        return (month - 1) * 30 + day_of_month

    def day_of_week(day):
        return ((day - 1) % 10) + 1

    def weekno(month, day):
        return ((day_of_year(month, day) - 1) // 10) + 1

----

More code features
==================

The syntax highlighting is done via docutils by a module called Pygments_
which support all popular languages, and a lot of unpopular ones as well.

The coloring is done by CSS, if you want to change it, copy the CSS in
the highlight.css file and override it in your custom CSS.

.. _Pygments: http://pygments.org/

----

Testing the code
================

If you are including Python-code, then Manuel_ 1.7.0 and later can test the
code for you. This enables you to have code in your presentation and make
sure it works.

To do this properly you sometimes want setup and teardown code, code that
should be executed as a part of the test, but not shown in the presentation.

To do that, you can simply set a class on the code block.

.. code:: python
    :class: hidden

    from datetime import datetime

Add the hidden class in your css:

.. code:: css

    pre.hidden {
        display: none;
    }

----

And your visible code will now be runnable with Manuel:

.. code:: python

   >>> datetime(2013, 2, 19, 12)
   datetime.datetime(2013, 2, 19, 12, 0)

.. _Manuel: http://pygments.org/

----

That's all folks!
=================

That finishes the basic tutorial for Hovercraft! Next you probably want to
take a look at the positioning tutorial, so you can use the pan, rotate and
zoom functionality.
