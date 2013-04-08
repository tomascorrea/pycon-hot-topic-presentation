:title: Pycon
:author: Jayson, Chacon e Tomas
:description: Apresentção dos principais pontos observados na PyCon US 2013.
:keywords: pycon
:css: pycon.css


PyCon US 2013 - Santa Clara - California
========================================

Principais pontos

----

Keynote do Guido
================

API de chamadas asyncronas em python
------------------------------------

.. code:: python

    import requests

    @coroutine
    def my_task(url):
        yield from requests.get(url)

----


Raspberry Pi
============

Cada participante ganhou um Raspberry Pi e foram dados vários workshops. Mudar o mundo através da educação. Levar tecnologia aos menos favorecidos.

----

The Naming of Ducks
===================

Where Dynamic Types Meet Smart Conventions
------------------------------------------

Em linguagens com tipagem estática o tipo da váriavel dá uma ideia do que uma variável, parâmetro ou retorno representa. Em linguagens com tipagem dinâmica precisamos dar bons
nomes as variáveis, classes e funções. O código abaixo demonstra quão difícil pode ser entender um código com nomes pouco representativos.


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


Salt Stack
==========

Salt Stack é uma ferramenta para gerenciamento de infraestrutura. O Salt pode funcionar no esquema
"master-minions" ou "masterless". Suas principais features são:

- Gerenciamento de configurações
- Execução remota de comandos
- Velocidade!

----

Docker
======

Docker complementa o LXC com uma API de alto nível que opera ao nível de processo. O Docker roda processos UNIX
com garantia de isolamento e repetitividade através de diversos servidores. Docker é uma boa ferramenta para a
automação de sistemas distribuidos como: deployments de larga escala, clusters de banco de dados, sistema de
deployment contínuo, PaaS privado, etc.


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


FPM
===

FPM é um construtor de pacotes para diversos formatos. Construa .deb, .rpm, .tar.* etc. com uma simples linha
de comando.

----

Parcel
======

Parcel é uma suite de classes e helpers desenhados para funcionarem em conjunto ao Fabric para a construção e
deployment de aplicações web Python usando pacotes nativos. Parcel é um projeto muito novo ainda suportando
somente pacotes Debian e CentOS e deployment com uWSGI.

----

Loggly
======

Loggly é um serviço de gerenciamento de logs. Com ele fica muito fácil armazenar, analisar, debugar, monitorar
e alertar com base nos logs de sua aplicação. Além de uma interface muito rica, o Loggly também suporta uma API
para a extração e visualização de seus logs.

Uma feature interessante do Loggly é sua integração com o New Relic, que deixa muito fácil achar os logs para
aquele pico na performance de sua aplicação.


----


Outros links
============


    - http://friggeri.net/blog/a-genetic-approach-to-css-compression/
    - http://cldr.unicode.org/
