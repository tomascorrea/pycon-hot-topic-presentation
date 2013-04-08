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

Solid Python Deployments for Everybody
======================================

#. http://ox.cx/d


----

    - FPM - Empacotador
    - pi-tools - https://github.com/nvie/pip-tools
    - parcel - http://parcel.readthedocs.org/en/latest/user/quickstart.html ( fabric + package)
    - fail2ban - segurança
    - icinga - monitoramento - https://www.icinga.org/
    - librato - estatisticas - https://metrics.librato.com


----


Mutant Tests
============


    Testando os testes e uma metrica melhor que coverage. Melhor que covarege por que minimiza os "side effects"


http://miketeo.net/wp/index.php/projects/python-mutant-testing-pymutester


.. code:: bash

    ~$ mutant-nosetest --mutant-path /project/myapp tests/mock_tests


----

Available Mutators in PyMuTester
================================


If-Condition Negation
---------------------

    This mutator mutates the test conditional clause in the if-statement, by negating the final results of the test with a not keyword.


Loop Skipping
-------------

This mutator mutates the bodies of for- and while-loops. A continue statement is inserted on every other loop iteration, and prevents the rest of the loop body from executing.

----


Outros links
============


    - http://friggeri.net/blog/a-genetic-approach-to-css-compression/
    - http://cldr.unicode.org/

