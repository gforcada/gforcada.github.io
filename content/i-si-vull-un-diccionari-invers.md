Title: I si vull un diccionari invers?
Date: 2008-10-16 19:42
Author: admin
Category: General
Tags: python
Slug: i-si-vull-un-diccionari-invers
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/07/python_logo.png" data-align="right" alt="Logotip del Python" />A la feina havia d'ordenar un diccionari pels valors (i no per les claus), però després volia accedir (per clau) a les dades sense haver d'estar iterant per tot el diccionari fins que trobés una clau que tenia per valor el valor pel que estava iterant (mola l'explicació eh :D

Doncs molt fàcil, crees un altre diccionari amb els elements al revés i així ja tens l'accés directe tant a la clau com al valor :)

O sigui:

    dict((v,k) for k,v in dictionary.items())

Fàcil oi?

<a href="http://mail.python.org/pipermail/python-list/2005-March/312376.html" target="_blank" rel="noopener">Trobat a la llista de Python</a> (del 2005!)
